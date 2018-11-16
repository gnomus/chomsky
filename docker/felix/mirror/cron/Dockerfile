FROM debian:stable

RUN apt update && apt install -y cron

RUN echo "* * * * * rsync -rtlvH --delete-after --delay-updates --safe-links --max-delete=1000 rsync://mirror.de.leaseweb.net/archlinux/ /mirror/ >> /proc/1/fd/1 2>&1" >> /etc/crontab


CMD "cron -f"
