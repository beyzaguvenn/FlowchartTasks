START

PRINT "Enter your ID number"
READ idNumber

PRINT "Identity verified"

LOOP
    PRINT "Select an action"
    PRINT "1 - Make Appointment"
    PRINT "2 - View Test Results"
    PRINT "3 - Exit"

    READ choice

    IF choice = 1 THEN
        CALL AppointmentModule
    ELSE IF choice = 2 THEN
        CALL TestResultsModule
    ELSE IF choice = 3 THEN
        PRINT "Exiting system"
        BREAK
    ELSE
        PRINT "Invalid selection"
    ENDIF
END LOOP

END



MODULE AppointmentModule

PRINT "Select Clinic"
READ clinic

PRINT "Displaying doctor list"
READ doctor

LOOP
    PRINT "Showing available time slots"
    READ timeSlot

    PRINT "Confirm appointment? (yes/no)"
    READ confirm

    IF confirm = "yes" THEN
        PRINT "Appointment confirmed"
        PRINT "SMS notification sent"
        BREAK
    ELSE
        PRINT "Select another time slot"
    ENDIF
END LOOP

RETURN



MODULE TestResultsModule

PRINT "Checking if tests exist"

IF testsExist = false THEN
    PRINT "No test records found"
    RETURN
ENDIF

PRINT "Checking if results are ready"

IF resultsReady = true THEN
    PRINT "Displaying test results"

    PRINT "Download results as PDF? (yes/no)"
    READ download

    IF download = "yes" THEN
        PRINT "PDF downloaded"
    ENDIF

ELSE
    PRINT "Results are not ready yet. Please wait."
ENDIF

RETURN
