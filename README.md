# Auto-sms

This is a script we use to send automated sms reminders to club leaders.

## Configuration

First, set up your Twilio information in `.twiliorc`

```bash
TWILIO_ACCOUNT_SID # your Twilio account SID
TWILIO_AUTH_TOKEN  # your Twilio auth token
TWILIO_CALLER_ID   # the Twilio 'from' phone number
```

Next, add clubs to the `CLUBS` array

```bash
# Club meeting data is formatted like this:
# "date +%u-%H-%M:leader_name:phone_number"
CLUBS=(
  # Send a message to Zaphod at 415-555-1212 on Monday, at 1:45PM
  "1-13-45:Zaphod:4155551212"
  # Send a message to Pat at 415-555-5555 on Tuesday, at 8:05AM
  "2-08-05:Pat:4155555555"
)
```
