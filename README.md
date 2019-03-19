This role pip-installs [rotate-backups](https://github.com/xolox/python-rotate-backups), configures it according to `rotate_targets`, and registers a cron task to run it on the `rotate_backups_cron` schedule.

~~~
rotate_backups_cron:
  minute: 7
  hour: '*'
  day: '*'
  month: '*'
  weekday: '*'

rotate_targets:
  - directory: "/backup"
    hourly: 24
    daily: 1
    weekly: 3
    monthly: 6
    yearly: always
    ionice: idle
~~~
