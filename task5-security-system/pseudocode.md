START Smart Home Security System

SET SystemActive = TRUE

WHILE SystemActive = TRUE

    Check system status
    IF system is not active THEN
        Wait and check again
    ELSE

        Read all sensors

        IF motion is detected THEN
            MotionThreat = TRUE
        ELSE
            MotionThreat = FALSE
        ENDIF

        IF door or window is opened unexpectedly THEN
            EntryThreat = TRUE
        ELSE
            EntryThreat = FALSE
        ENDIF

        IF MotionThreat OR EntryThreat THEN

            Check if homeowner is at home

            IF homeowner is at home THEN
                PossibleFalseAlarm = TRUE
                AlarmLevel = 1
            ELSE
                PossibleFalseAlarm = FALSE

                IF motion AND entry detected THEN
                    AlarmLevel = 3
                ELSE
                    AlarmLevel = 2
                ENDIF

            ENDIF

            IF AlarmLevel >= 2 THEN
                Activate security camera
            ENDIF

            Send notifications to homeowner
            (SMS + Mobile App + Email)

        ENDIF

        Wait a short period

        Check if reset command is received
        IF reset command received THEN
            Reset alarm state
        ENDIF

    ENDIF

ENDWHILE
