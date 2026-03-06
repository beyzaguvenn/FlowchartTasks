START

Student logs into the system

IF login is valid THEN

    Display available course list

    WHILE student wants to select a course DO

        Student selects a course

        IF course quota is available THEN

            IF prerequisites are satisfied THEN

                IF no schedule conflict with selected courses THEN

                    IF credit limit is not exceeded THEN

                        Add course to temporary selection list

                    ELSE
                        Reject course (credit limit exceeded)

                    ENDIF

                ELSE
                    Reject course (schedule conflict)

                ENDIF

            ELSE
                Reject course (prerequisites not completed)

            ENDIF

        ELSE
            Reject course (quota full)

        ENDIF

    ENDWHILE

    IF advisor approval is required THEN

        Send courses to advisor

        IF advisor approves THEN
            Confirm registration
        ELSE
            Registration rejected
        ENDIF

    ELSE
        Confirm registration
    ENDIF

ELSE
    Login failed

ENDIF

END
