# Cronjob

Cronjob is used to run commands programmatically

## Crontab command

Use `crontab -e` to set up a cron job

## Cronjob syntax

`a b c d e command`

`a` --> minute 0-59  
`b` --> hour 0-23  
`c` --> day 1-31  
`d` --> month 1-12  
`e` --> day of week 0-6

Run the command every time the date matches the following specification  
Run the command every time the clock shows 30 minutes  
`30 * * * * command`

Run a job every monday in April at 6:30AM  
`30 6 * 4 1 command`

Run a job at midnight on the first of every month  
`0 0 1 * * command`

Run a job at midnight every weekday  
`0 0 * * 1-5 command`

Run a job every 5 minutes  
`*/5 * * * * command`

Website to help setting up cron jobs: https://crontab.guru
