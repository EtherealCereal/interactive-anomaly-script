# interactive-anomaly-script

Purpose of the script is to run some detectable events that have unique names (not arguments) and appear to be triggered interactively in a tty session.
Running into issues with the script not appearing to run properly from cron.

runscript on ubuntu 20.04 or similar.
copy to bin and chmod +x

run the script `anomaly`

Creates 10 randomly named events (+1 uncaught anomalous event) and triggers them with a newly created ssh connection. The events are renamed copies of `echo`

------------------
What doesn't work:
------------------

* The script needs to be run from cron everyday without a human having to login to the instance and trigger it.  
      currently the script runs from crontab, but the scripts that need to be interactive (have tty) aren't showing running as interactive.
* add_user currently unable to run the script as a newly created user and the script doesn't exit out of the new user

