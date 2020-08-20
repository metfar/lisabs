# lisabs

LISABS - LIghtweight Scheduling And Backup System


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
