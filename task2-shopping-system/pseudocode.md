START

START USER LOGIN
    LOOP
        User enters login credentials
        IF credentials are valid THEN
            Login successful
            EXIT LOOP
        ELSE
            Ask user to try again
        ENDIF
    ENDLOOP
END

START SHOPPING
    LOOP
        User selects product

        IF product is in stock THEN
            Add product to cart
        ELSE
            Notify product unavailable
        ENDIF

        IF user wants to continue shopping THEN
            Continue LOOP
        ELSE
            EXIT LOOP
        ENDIF
    ENDLOOP
END

START DISCOUNT CODE
    IF user has discount code THEN
        IF code is valid THEN
            Apply discount
        ELSE
            Ignore discount code
        ENDIF
    ENDIF
END

START SHIPPING CALCULATION
    IF cart total > free shipping limit THEN
        Shipping fee = 0
    ELSE
        Add standard shipping fee
    ENDIF
END

START PAYMENT
    LOOP
        User attempts payment

        IF payment successful THEN
            Confirm order
            EXIT LOOP
        ELSE
            Ask user to retry payment
        ENDIF
    ENDLOOP
END

END
