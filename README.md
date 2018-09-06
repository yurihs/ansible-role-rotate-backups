This role pip-installs [rotate-backups](https://github.com/xolox/python-rotate-backups), configures it according to `rotate_retention_config`, and registers a cron task to run it on the `rotate_backups_cron` schedule.

~~~
rotate_backups_cron:
  minute: 7
  hour: '*'
  day: '*'
  month: '*'
  weekday: '*'

rotate_target_directory: "/backup"

rotate_retention_config:
  hourly: 24
  daily: 1
  weekly: 3
  monthly: 6
  yearly: always
  ionice: idle
~~~
