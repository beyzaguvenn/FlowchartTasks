START
    SET DailyLimit = 5000
    SET DailyWithdrawn = 0
    SET PinAttempts = 0
    SET MaxAttempts = 3
    SET AccountBalance = 10000

    LOOP WHILE PinAttempts < MaxAttempts
        PRINT "Please enter your PIN:"
        READ UserPin
        
        IF UserPin IS Correct THEN
            PRINT "Access Granted."
            BREAK LOOP (Go to Transaction Menu)
        ELSE
            SET PinAttempts = PinAttempts + 1
            PRINT "Incorrect PIN. Attempts remaining: " + (MaxAttempts - PinAttempts)
            
            IF PinAttempts == MaxAttempts THEN
                PRINT "Card Blocked. Please contact your bank."
                END
            END IF
        END IF
    END LOOP

    LABEL TransactionMenu
    PRINT "Enter withdrawal amount (multiples of 20TL):"
    READ WithdrawalAmount

    IF (WithdrawalAmount MOD 20) != 0 THEN
        PRINT "Error: Amount must be a multiple of 20TL."
        GOTO TransactionMenu
    ELSE IF WithdrawalAmount > AccountBalance THEN
        PRINT "Error: Insufficient funds."
        GOTO TransactionMenu
    ELSE IF (WithdrawalAmount + DailyWithdrawn) > DailyLimit THEN
        PRINT "Error: Daily limit exceeded."
        GOTO TransactionMenu
    ELSE
        SET AccountBalance = AccountBalance - WithdrawalAmount
        SET DailyWithdrawn = DailyWithdrawn + WithdrawalAmount
        PRINT "Dispensing Cash..."
        PRINT "New Balance: " + AccountBalance
    END IF

    PRINT "Would you like another transaction? (Yes/No)"
    READ UserChoice
    IF UserChoice == "Yes" THEN
        GOTO TransactionMenu
    ELSE
        PRINT "Please take your card. Goodbye!"
        END
    END IF
END
