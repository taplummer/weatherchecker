# Weather Checker for Linux

This is a bash script to pull the weather forecast for the day and push a desktop notification to your computer at 8 AM each work day.

If you run this script later in the day, you may get the next day's forecast in lieu of the current day's forecast. 

## Installation

***Note: When you are using the installer, do not use any punctuation. The first argument is your city and the second argument is your state's abbreviation. If your city has two or more names, the names should be separated by a hyphen as shown below***

```git clone ```

```cd weatherchecker```

```./installer your-city tx```

## Modifying Crontab

```crontab -e```

This will pull up your user-specfic crontab. 

The installer script should've entered ```0 8 * * 1-5 XDG_RUNTIME_DIR=/run/user/$(id -u) bash ~/.weather your-city ca```

On some distros, you may need to change the ```XDG_RUNTIME_DIR=/run/user/$(id -u)``` part. Unfortunately, it's a bit of trial and error with cron pushing notifications, so your mileage may vary if the included configuration doesn't work.
