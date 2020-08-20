# Application

    LISABS - LIghtweight Scheduling And Backup System

                This application is made to realize 
                periodically backups, compressed or not, 
                and store into a designated location.
    
    LISABS requires arguments
    
    -h|-?               Shows this help
    
    --execute           Makes a backup (first parameter only)
    -g|--get            Gets execution cron information
    -i|--info           Show all setted options
    -l|--list           Lists all the files/dirs that are 
                        configured to be backuped.
    
    -aName1:name2···    Adds one or more files/directories names
    --addName1:name2··· separated by ':' into the list.
    
    -eName1:name2···    Erase one or more files/directories names
    --delName1:name2··· separated by ':' from the list.
    
                        
    -n[0-9]             Sets the number of backups to keep 
						(2 implies {0,1,2} backups)
    -C|--compress       Enables compression
    -m38|--minute38     Set backup to minute 38
    -h13|--hour13       Set to start the backup at 1 pm
    -D5|--day5          Start backup on 5th day of the month
    -M7|--month7        Start backup on 7th month
    -d3|--dow3          Start backup on day 3rd of the week
    
    -s|--schedule       Adds this backup event to crontab 
    -u|--unschedule     Delete LISABS from crontab
    
    -A|--anytime        Set time to any time 
                        (clean setted time options)
    
    
    --each-minute15     Set minutes to each quarted of hour (*/15)
    --each-hour3        Set hour to each third hour
    --each-day5         Set days to each fifth day
    --each-month2       Set month to each second month
    
    
    -w'/tmp/Backup'     Set backups' saving location to /tmp/Backup
    
    
                            metfar@gmail.com
    


# License
##
  Copyright 2020 William Martinez Bas <metfar@gmail.com>

  This program is free software; you can redistribute it and/or modify
  it under the terms of the GNU General Public License as published by
  the Free Software Foundation; either version 2 of the License, or
  (at your option) any later version.
  
  This program is distributed in the hope that it will be useful,
  but WITHOUT ANY WARRANTY; without even the implied warranty of
  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
  GNU General Public License for more details.
  
  You should have received a copy of the GNU General Public License
  along with this program; if not, write to the Free Software
  Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston,
  MA 02110-1301, USA.
  Proposal: Make a local backup scheme using rsync. You can try to compress it and schedule it using crontab. 

# Configuration

## The configuration file will have the same name as the script.

#!/bin/cat 
Temp="/tmp/"  #temporal directory
Backups="2"   #copies to keep - 1
Actual="2"    #last copy number
Compress="1"  #1=Yes=True   0=False
LastBackup="2020.08.20.08.58" #Last dateTime in format YYYY.MM.DD.HH.mm
Minute="*/5"  #each 5 minuts
Hour="*"    #any hour
DayOfMonth="*" #any day
Month="*" #any month
DayOfWeek="*" #any week
Which=" /etc/fstab:/home/thisUser/.LISABS" #files to store
Where="/tmp/SaveBackupsHere/" #where to save the backups


# Regards

William Martinez Bas ( metfar@gmail.com )
