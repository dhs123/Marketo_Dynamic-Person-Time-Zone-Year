# Marketo_Dynamic-Person-Time
This repository contains the velocity script for displaying the correct year in the emails in marketo emails.

How to use?

The [velocity script](https://github.com/dhs123/Marketo_Dynamic-Person-Time/blob/main/person_time_zone_VS) contains the code snippet to display the year dynamically in an email. 

Instructions for adding code in Marketo Emails:
1. Copy the velocity script.
2. Create a new email-script token in Marketo preferably at the highest program/campaign folder level. (Goto the "My Tokens" tab of a program/campaign folder and drag the email script token from the right into the canvas).
3. Paste the copied script in the email-script token. Make sure to read the additional notes below before saving the script token.
4. Add the custom my token in the email asset/template.

Additional Notes for using and modifying the velocity script:

1. Update the fall-back/default timezone in the $defaultTimeZone field (currently it is set to "Asia/Kolkata") as per the "[IANA time zone List](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones#List)".

2. "$lead.Person_Time_Zone" field is the system-managed time zone field. Make sure to checkmark the field from the tree on right of the email-script editor so that its data is available to the script. 

![image](https://user-images.githubusercontent.com/20539123/210195092-29765b6d-f4b5-4b41-a4e1-0033f5ca7f97.png)

3. "$lead.customTimeZone" is a custom time zone field. Make sure to update the field name in the script with the field specific to your instance. If you do not have a custom field for storing the person time zone created in your instance, then you could remove it from the code.
