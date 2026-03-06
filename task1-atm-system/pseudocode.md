START

SET attempts = 0
SET correctPIN = 1234
SET balance = 5000
SET dailyLimit = 2000
SET withdrawnToday = 0

LOOP while attempts < 3

    PRINT "Enter your PIN:"
    READ pin

    IF pin = correctPIN THEN
        PRINT "PIN correct"

        LOOP

            PRINT "Enter withdrawal amount:"
            READ amount

            IF amount % 20 ≠ 0 THEN
                PRINT "Amount must be multiple of 20 TL"

            ELSE IF amount > balance THEN
                PRINT "Insufficient balance"

            ELSE IF withdrawnToday + amount > dailyLimit THEN
                PRINT "Daily withdrawal limit exceeded"

            ELSE
                balance = balance - amount
                withdrawnToday = withdrawnToday + amount
                PRINT "Please take your cash"
                PRINT "New balance:", balance
            ENDIF

            PRINT "Do you want another transaction? (yes/no)"
            READ choice

            IF choice = "no" THEN
                PRINT "Thank you for using the ATM"
                STOP
            ENDIF

        END LOOP

    ELSE
        attempts = attempts + 1
        PRINT "Incorrect PIN"

        IF attempts = 3 THEN
            PRINT "Card blocked"
            STOP
        ENDIF

    ENDIF

END LOOP

END
