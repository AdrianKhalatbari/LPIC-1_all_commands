# LPIC-1 Commands Reference

> Created by **Mohammad Mahdi Khalatbari**

---

## Table of Contents

- [101.1 — Determine and configure hardware settings](#1011--determine-and-configure-hardware-settings)
- [101.2 — Boot the system](#1012--boot-the-system)
- [101.3 — Change runlevels and shutdown or reboot system](#1013--change-runlevels-and-shutdown-or-reboot-system)
- [102.1 — Design hard disk layout](#1021--design-hard-disk-layout)
- [102.2 — Install a boot manager](#1022--install-a-boot-manager)
- [102.3 — Manage shared libraries](#1023--manage-shared-libraries)
- [102.4 — Use Debian package management](#1024--use-debian-package-management)
- [102.5 — Use RPM and YUM package management](#1025--use-rpm-and-yum-package-management)
- [103.1 — Work on the command line](#1031--work-on-the-command-line)
- [103.2 — Process text streams using filters](#1032--process-text-streams-using-filters)
- [103.3 — Perform basic file management](#1033--perform-basic-file-management)
- [103.4 — Use streams, pipes and redirects](#1034--use-streams-pipes-and-redirects)
- [103.5 — Create, monitor and kill processes](#1035--create-monitor-and-kill-processes)
- [103.6 — Modify process execution priorities](#1036--modify-process-execution-priorities)
- [103.7 — Search text files using regular expressions](#1037--search-text-files-using-regular-expressions)
- [103.8 — Perform basic file editing operations using vi](#1038--perform-basic-file-editing-operations-using-vi)
- [104.1 — Create partitions and filesystems](#1041--create-partitions-and-filesystems)
- [104.2 — Maintain the integrity of filesystems](#1042--maintain-the-integrity-of-filesystems)
- [104.3 — Control mounting and unmounting of filesystems](#1043--control-mounting-and-unmounting-of-filesystems)
- [104.4 — Manage disk quotas](#1044--manage-disk-quotas)
- [104.5 — Manage file permissions and ownership](#1045--manage-file-permissions-and-ownership)
- [104.6 — Create and change hard & symbolic links](#1046--create-and-change-hard--symbolic-links)
- [104.7 — Find system files and place files in the correct location](#1047--find-system-files-and-place-files-in-the-correct-location)
- [105.1 — Customize and use the shell environment](#1051--customize-and-use-the-shell-environment)
- [105.2 — Customize or write simple scripts](#1052--customize-or-write-simple-scripts)
- [105.3 — SQL data management](#1053--sql-data-management)
- [106.1 — Install and configure X11](#1061--install-and-configure-x11)
- [106.2 — Setup a display manager](#1062--setup-a-display-manager)
- [106.3 — Accessibility](#1063--accessibility)
- [107.1 — Manage user and group accounts](#1071--manage-user-and-group-accounts)
- [107.2 — Automate system administration tasks by scheduling jobs](#1072--automate-system-administration-tasks-by-scheduling-jobs)
- [107.3 — Localisation and internationalisation](#1073--localisation-and-internationalisation)
- [108.1 — Maintain system time](#1081--maintain-system-time)
- [108.2 — System logging](#1082--system-logging)
- [108.3 — Mail Transfer Agent (MTA) basics](#1083--mail-transfer-agent-mta-basics)
- [108.4 — Manage printers and printing](#1084--manage-printers-and-printing)
- [109.1 — Fundamentals of internet protocols](#1091--fundamentals-of-internet-protocols)
- [109.2 — Basic network configuration](#1092--basic-network-configuration)
- [109.3 — Basic network troubleshooting](#1093--basic-network-troubleshooting)
- [109.4 — Configure client side DNS](#1094--configure-client-side-dns)
- [110.1 — Perform security administration tasks](#1101--perform-security-administration-tasks)
- [110.2 — Setup host security](#1102--setup-host-security)
- [110.3 — Securing data with encryption](#1103--securing-data-with-encryption)

---

## 101.1 — Determine and configure hardware settings

| Command | Description |
|---------|-------------|
| `ls /dev` | تمام دیوایس های سیستم در اینجا قابل مشاهده هستند |
| `ls /sys` | لیست فایل های مربوط به دستگاه های سخت افزاری سیستم |
| `ls /proc` | لیست فایل های اطلاعاتی پروسس ها و هسته سیستم |
| `cat /proc/cpuinfo` | اطلاعات مربوط به پردازنده سیستم |
| `cat /proc/meminfo` | اطلاعات مربوط به رم سیستم |
| `/proc/sys/fs` | تنظیمات هسته لینوکس در اینجا قرار دارد |
| `cd /proc/sys/net` | تمام فایل ها و تنظیمات مربوط به شبکه اینجا قرار دارد |
| `ls /dev/sda*` | نمایش تمام پارتیشن های دیسک اول |
| `lsmod` | لیست ماژول هایی که کرنل لود کرده است |
| `rmmod <module name>` | پاک کردن ماژول |
| `modprobe <module name>` | اضافه کردن ماژول |
| `lsusb` | تمام دیوایس هایی که از طریق یو اس بی وصل هستند |
| `lspci` | تمام دستگاه هایی که از طریق بی سی ای وصل هستند |
| `lshw -short` | تمام اطلاعات سخت افزاری سیستم را به صورت کامل نشان میدهد |

---

## 101.2 — Boot the system

| Command | Description |
|---------|-------------|
| `/boot/grub/grub.cfg` | فایل کانفیگ اصلی grub2 که تنظیمات بوت در آن قرار دارد |
| `pstree` | نمایش درختی تمامی پروسس ها |
| `/var/log/dmesg` | تمامی لاگ های خود کرنل |
| `/var/log/messages` | برای دیدن دقیق تر لاگ های سیستم |
| `/var/log/syslog` | همانند دستور بالا |
| `var/log/boot.log` | برای دیدن لاگ ها تا پایان بوت |

---

## 101.3 — Change runlevels and shutdown or reboot system

| Command | Description |
|---------|-------------|
| `runlevel` | برای مشاهده سطح اجرایی حال حاضر |
| `telinit 5` | برای تغییر سطح اجرایی |
| `ls /etc/rc2.d/` | فایل هایی که سرویس های هر سطح اجرایی را نمایش میدهند |
| `shutdown -r 60 Reloading updated kernel` | ریبوت سیستم بعد از ۶۰ ثانیه با نمایش پیام به کاربران |
| `shutdown -c` | دستور خاموش شدن را کنسل می کند |
| `initctl list` | وضعیت هر کدام از ایونت ها را نمایش میدهد و فقط مخصوص دبیان است |
| `systemctl` | وضعیت هر کدام از یونیت ها را نمایش میدهد که مخصوص ردهت می باشد |

---

## 102.1 — Design hard disk layout

| Command | Description |
|---------|-------------|
| `fdisk /dev/sda` | برای مدیریت دیسک های MBR |
| `p` | نمایش پارتیشن ها |
| `q` | خروج |
| `parted /dev/sda p` | برای مدیریت دیسک های GPT |

---

## 102.2 — Install a boot manager

| Command | Description |
|---------|-------------|
| `/etc/lilo.conf` | فایل تنظیمات lilo |
| `/usr/sbin/liloconfig` | برای ساخت فایل lilo.conf |
| `lilo -v` | نصب lilo |
| `/boot/grub/grub.conf` | کانفیگ فایل grub |
| `grub-install /dev/fd0` | نصب grub |
| `/boot/grub/grub.cfg` | فایل کانفیگ grub2 |
| `grub-install /dev/sda` | نصب grub2 |

---

## 102.3 — Manage shared libraries

| Command | Description |
|---------|-------------|
| `ls /lib` | مشاهده کتابخانه های ۳۲ بیتی سیستم |
| `ls /lib64` | مشاهده کتابخانه های ۶۴ بیتی سیستم |
| `ls /usr/lib` | مشاهده لیب های سیستم |
| `ldd <program address>` | مشاهده لیب های مورد استفاده یک برنامه |
| `locate <file name>` | برای گرفتن ادرس یک فایل در لینوکس |
| `cat /etc/ld.so.conf` | محل تمامی فایل های کانفیگ در اینجا قرار دارد |
| `ldconfig` | مسیر همه لیب ها را در فایل ld.so.catch ذخیره میکند |
| `ldconfig -p` | مشاهده تمامی لیب هایی که در دستور بالا ذخیره شده اند — تمام لیب های لود شده سیستم عامل |
| `ls.so.catch` | حاوی مسیر همه لیب ها |
| `export LD_LIBRARY_PATH=/usr/lib/myoldlibs` | در صورت اضافه کردن لیب به لینوکس آن را با این دستور به سیستم میشناسانیم |

---

## 102.4 — Use Debian package management

> `bzr` is an app name used in examples below.

| Command | Description |
|---------|-------------|
| `which bzr` | برنامه کجا قرار دارد |
| `whereis bzr` | آدرس برنامه کجاست |
| `apt-get install -s bzr` | نصب به صورت simulate |
| `apt-get install --download-only bzr` | فقط دانلود کند و نصب نکند |
| `cat /etc/apt/sources.list` | آدرس تمامی repository |
| `apt-get remove bzr` | پاک کردن فقط برنامه |
| `apt-get autoremove bzr` | پاک کردن یک برنامه به همراه فایل های وابسته |
| `apt-get autoremove` | این دستور به صورت خودکار برنامه های اضافی که وابسته بوده اند را تشخیص داده و حذف میکند |
| `apt-cache search "tiny window"` | برای جستجو |
| `aptitude search grub2` | برای جستجو |
| `apt-get update` | برای اپدیت کردن repositories |
| `apt-get upgrade` | برای آپگرید کردن برنامه ها |
| `apt-get dist-upgrade` | برای اپگرید کل سیستم عامل به نسخه جدید |
| `dpkg reconfigure tzdata` | تنظیمات دوباره یک برنامه |
| `dpkg contents bzr.deb` | محتوی یک فایل دبیان |
| `dpkg -s bzr.deb` | وضعیت بسته ها را نمایش می دهد |
| `dpkg -P bzr.deb` | آثار یک برنامه را کاملا حذف می کند |
| `dpkg -L bzr.deb` | تمام برنامه ها و لیب هایی که نصب کرده است را می گوید |
| `dpkg -S /usr/share/jcal` | چه برنامه ای این را نصب کرده است |
| `dpkg -i bzr.deb` | نصب یک فایل deb به صورت مستقل |
| `aptitude` | رابط کاربری تعاملی برای مدیریت بسته های دبیان |

---

## 102.5 — Use RPM and YUM package management

| Command | Description |
|---------|-------------|
| `/etc/yum.repo.d` | لیست تمامی repository |
| `/etc/yum.conf` | فایل کانفیگ yum |
| `rpm -i bzr.rpm` | نصب یک بسته از فایل rpm — بدون نصب فایل های وابسته |
| `rpm -U bzr.rpm` | آپگرید یا نصب یک پکیج |
| `rpm -F bzr.rpm` | اگر فایل نصب شده ورژن پایین تر این فایل بود آپگرید میکند در غیر اینصورت کاری نمی کند |
| `rpm -e bzr` | پاک کردن برنامه بدون حذف فایل های وابسته |
| `yum install bzr` | نصب یک بسته از طریق repository — به همراه نصب فایل های وابسته |
| `yum autoremove bzr` | پاک کردن به همراه حذف فایل های وابسته |
| `yum upgrade 'cal*'` | آپگرید یک برنامه خاص یا کل برنامه های سیستم |
| `yum reinstall bzr` | نصب مجدد یک بسته که قبلاً نصب شده است |
| `yum deplist jcal` | کل فایل های وابسته این برنامه را نمایش میدهد |
| `yumdownloader --resolve bzr` | فقط دانلود میکند به همراه دانلود فایل های وابسته |

**Querying info:**

| Command | Description |
|---------|-------------|
| `yum list bzr` | اطلاعات یک پکیج را نمایش میدهد |
| `rpm -q bzr` | اطلاعات یک پکیج rpm را نمایش میدهد |
| `yum info bzr` | هر سه دستور بالا برای گرفتن اطلاعات یک پکیج می باشد |
| `yum search hack` | تمام پکیج هایی که شامل هک می باشد را نمایش می دهد |
| `rpm -qa` | تمام پکیج های نصب شده را نمایش میدهد |
| `rpm -ql bzr` | لیست تمام پکیج هایی که این بسته نصب کرده است را نمایش می دهد |
| `rpm -qR bzr` | پکیج های مورد نیاز برای نصب این برنامه |
| `rpm -qF /usr/share/test.mo` | برای دیدن اینکه یک فایل را چه برنامه ای نصب کرده است |

**Integrity:**

| Command | Description |
|---------|-------------|
| `rpm -vK bzr.rpm` | آیا این همان بسته است که نصب شده است |
| `rpm -V bzr` | آیا بسته های نصب شده تطابق دارند؟ |

---

## 103.1 — Work on the command line

| Command | Description |
|---------|-------------|
| `/etc/profile` | محل قرار گیری فایل های کانفیگ shell |
| `echo Hello lpic` | نمایش یک متن در خروجی ترمینال |
| `echo line 1;echo line 2` | اول دستور سمت چپ و بعد دستور سمت راست را اجرا می کند |
| `echo line 1 && echo line 2` | اگر دستور سمت چپ درست انجام شد بعد دستور سمت راست را اجرا کن |
| `echo line 1 \|\| echo line 2` | اگر دستور سمت راست اجرا شد دستور سمت چپ را اجرا نکن |
| `bash` | در همان بش یک بش جدید باز میکند |
| `exec ls` | بعد از اجرا دستور بش را می بندد |
| `echo -e "hi\nhosareyou"` | این سوئیچ برای زمانی است که میخواهیم کاراکتر های خاص را بش بفهمد |

**Environment Variables:**

| Command | Description |
|---------|-------------|
| `echo $USER` | نمایش نام کاربر فعلی |
| `echo $UID` | نمایش شناسه عددی کاربر فعلی |
| `echo $HOME` | آدرس دایرکتوری HOME را نشان میدهد |
| `echo $SHELL` | آدرس شل را میدهد |
| `echo $PWD` | دایرکتوری فعلی را نمایش می دهد |
| `echo $$` | شناسه پروسس جاری |
| `echo $PPID` | شناسه پروسس والد |
| `echo $?` | اگر مقدار آن صفر بود یعنی از دستور قبلی درست خارج شده است |
| `MYMOOD=happy` | تعریف یک متغیر محلی در شل |
| `export MYMOOD` | یعنی از اینجا به بعد هر برنامه ای که در بش ران شود به این متغیر دسترسی دارد |
| `echo $MYMOOD` | نمایش مقدار متغیر تعریف شده |
| `env` | نمایش تمام متغیر های محیطی |
| `set` | نمایش تمام متغیر های محیطی |
| `unset CHERT` | متغیر محیطی را حذف می کند |
| `uname -a` | تمام اطلاعات در مورد سیستم عامل مورد نظر را به ما میدهد |

**History:**

| Command | Description |
|---------|-------------|
| `history` | تاریخچه دستورات اجراشده را میدهد |
| `history 20` | نمایش ۲۰ دستور آخر اجراشده |
| `!!` | آخرین دستور اجرا شده را مجددا اجرا میکند |
| `!echo` | آخرین دستوری که در آن اکو هست را مجددا اجرا میکند |
| `ctrl+r` | دستورات قبلی را نمایش میدهد و قابلیت جستجو دارد |

**PATH:**

| Command | Description |
|---------|-------------|
| `echo $PATH` | مشاهده نمامی پت ها |
| `PATH=$PATH:/usr/temp` | آدرس جدید را به پت های قبلی اضافه میکند |
| `/etc/profile` | برای اضافه کردن یک پت به سیستم باید این فایل را تغییر دهیم |
| `man ping` | مشاهده manual هر دستور |
| `which ping` | کجاست |
| `whereis ping` | کجاست |
| `type ping` | چیست |

---

## 103.2 — Process text streams using filters

| Command | Description |
|---------|-------------|
| `ls -1 \| sort (-r)` | هر خروجی در یک خط با منفی یک مشخص می گردد |
| `ls -ltrh > directory_data` | خروجی دستور ls را به فایل هدایت میکند (ریدایرکت) |
| `cat mydata directory_data` | در ابتدا فایل سمت چپ را نمایش میدهد و در ادامه فایل سمت راست |
| `cat mydata - directory_data` | این فایل ابتدا سمت چپ را نمایش میدهد و بعد منتظر ورودی از کاربر می ماند و بعد فایل سمت راست را نمایش میدهد |
| `ls \|cat what_i_have.txt - > sortedlist.txt` | محتوای فایل و خروجی ls را با هم ترکیب کرده در فایل جدید ذخیره میکند |

**od — dump files in octal and other formats:**

| Command | Description |
|---------|-------------|
| `od -Ad` | نمایش محتوای فایل به صورت اعشاری (decimal) |
| `od -Ao` | نمایش محتوای فایل به صورت اکتال (octal) |
| `od -Ax` | نمایش محتوای فایل به صورت هگزادسیمال (hex) |
| `od -Ad -ta` | نمایش فقط نام کاراکترها |
| `od -Ad -c` | نمایش کاراکترها به شکل قابل خواندن |

**split, wc, head, tail:**

| Command | Description |
|---------|-------------|
| `split -l 2 mydata` | سه خط سه خط جدا کرده و در فایل های جدیدی ذخیره میکند |
| `split -b 40 mydata` | چهل بایتی جدا میکند |
| `wc * mydata` | کاراکتر — کلمه — خط |
| `wc -l mydata` | نمایش تعداد لاین ها |
| `head -n 6 mydata` | شش خط بالای فایل را نمایش میدهد |
| `tail -n 6 mydata` | شش خط آخر را نمایش میدهد |
| `tail -f /var/log/syslog` | فایل لاگ را باز نگه داشته و به صورت آنلاین تغییرات را نمایش میدهد |

**Text processing:**

| Command | Description |
|---------|-------------|
| `expand mydata \| od -tc` | تمام تب ها را با اسپیس عوض میکند |
| `cat mydata \| tr '1' '2'` | همه یک ها را با دو عوض میکند |
| `pr mydata` | آماده سازی فایل متنی برای چاپ با صفحه بندی |
| `nl mydata` | نمایش فایل به همراه شماره خطوط |
| `fmt -rw80 mydata` | فرمت فایل ما را تغییر میدهد |
| `sort mydata` | مرتب سازی خطوط فایل (با -n برای مرتب سازی عددی) |
| `sort mydata \| uniq -c` | تعداد تکرار را نمایش میدهد |
| `sort mydata \| uniq -u` | تکراری ها را حذف کرده و بقیه را نمایش میدهد |
| `sort mydata \| uniq -d` | فقط تکراری ها را نمایش میدهد |
| `cut -f1 mydata` | قسمت عمودی از فایل را نمایش میدهد |
| `paste mydata uses` | خط اول فایل دوم را پشت خط اول فایل اول میگذارد و بقیه هم به همین ترتیب |
| `sort howcool > howcool.sorted` | مرتب سازی فایل howcool و ذخیره نتیجه |
| `sort uses > uses.sorted` | مرتب سازی فایل uses و ذخیره نتیجه |
| `join howcool.sorted uses.sorted` | برای این دستور ابتدا باید هر دو لیست را مرتب کنیم و بعد این دستور مقادیر مشترک را به ما نمایش میدهد |
| `sed 's/ubuntu/debian/g' uses` | مقادیر اوبونتو را با دبیان عوض می کند |

---

## 103.3 — Perform basic file management

| Command | Description |
|---------|-------------|
| `ls -ltrh` | l(list), t(time sorting), r(reverse), h(MB) |
| `cp sources destination` | کپی چند فایل در یک مقصد |
| `cp -f sources destination` | فایل را سریعا پاک میکند |
| `cp -i sources destination` | قبل از انجام فرآیند سوال میپرسد |
| `cp -b sources destination` | از فایل اصلی بکاپ گرفته و بعد آنرا کپی می کند |
| `cp -p sources destination` | تمامی تنظیمات همچون دسترسی ها را نیز کپی می کند |
| `cp -r mydir newCopy` | خودش و همه فرزندانش را کپی میکند |
| `mv source destination` | انتقال یا تغییر نام یک فایل یا دایرکتوری |
| `mv dir1 dir2` | move dir1 to dir2 and delete dir1 (this is rename) |
| `rm dir1` | حذف یک فایل یا دایرکتوری |
| `mkdir dirA dirB` | ساخت چند دایرکتوری به صورت همزمان |
| `mkdir -p newDir/insideNew/lastDir` | parent را هم میسازد |
| `rmdir dirA dirB` | حذف دایرکتوری های خالی |
| `tree` | نمایش درختی ساختار دایرکتوری ها و فایل ها |
| `rm newfile` | حذف یک فایل |
| `rm -r newDirectory` | حذف یک دایرکتوری به همراه تمام محتوای داخل آن |
| `rm *` | حذف تمام فایل های دایرکتوری جاری |
| `ls A*B` | نمایش تمام فایل هایی که با A شروع و با B تمام می شوند |
| `cp ???.* /tmp` | کپی تمام فایل هایی که نام آن ها ۳ کاراکتر دارد سپس نقطه و هر چیزی به tmp/ |
| `rmdir [a-z]*` | حذف تمام دایرکتوری هایی که با یک حرف کوچک شروع می شوند |

**touch:**

| Command | Description |
|---------|-------------|
| `touch -t 200908121510.59 f3` | زمان فایل را بصورت کامل میدهیم و آن را تغییر میدهد |
| `touch -d 11am f4` | تغییر زمان فایل به ساعت ۱۱ صبح امروز |
| `touch -d "last fortnight" f5` | به چهارده روز قبل تغییر میدهد |
| `touch -d "yesterday 6am" f6` | تغییر زمان فایل به دیروز ساعت ۶ صبح |
| `touch -d "2 days ago 12:00" f7` | تغییر زمان فایل به دو روز پیش ساعت ۱۲ |
| `touch -d "tomorrow 02:00" f8` | تغییر زمان فایل به فردا ساعت ۲ بامداد |
| `touch -d "5 Nov" f9` | تغییر زمان فایل به پنجم نوامبر |
| `touch -r f1 f1a` | تاریخ فایل سمت راست را به تاریخ فایل سمت چپ تغییر میدهد |

**Finding:**

| Command | Description |
|---------|-------------|
| `find . -iname "[a-j]*"` | جستجوی فایل هایی که نام آن ها با حروف a تا j شروع می شود (بدون حساسیت به بزرگی/کوچکی) |
| `find . -name "*my*"` | جستجوی فایل هایی که در نام آن ها my وجود دارد |
| `find . -type f -iname "*my*"` | جستجوی فایل (نه دایرکتوری) که my در نامشان باشد |
| `find . -type d -iname "*my*"` | جستجوی دایرکتوری که my در نامشان باشد |
| `find . -type l -iname "*my*"` | جستجوی لینک سمبولیک که my در نامشان باشد |
| `find /var -iname '*tmp*' -size (+or-)1M` | جستجوی فایل هایی با tmp در نام و اندازه بیشتر یا کمتر از ۱ مگابایت |
| `find . -atime -6 -exec rm '{}' \;` | بر اساس ساعت — آخرین باری که به فایل دسترسی داشتیم |
| `find . -ctime +6 -print \;` | آخرین باری که فایل را change کردیم |
| `find . -mtime 6 -ls \;` | آخرین باری که محتوی را عوض کردیم |
| `find . -mmin 20 -exec rm '{}' \;` | بر اساس دقیقه |
| `file /bin/bash` | نمایش نوع فایل |

**Compressing:**

| Command | Description |
|---------|-------------|
| `gzip The.Equalizer.srt` | خود فایل zip میشود و فایل اصلی حذف می شود |
| `gunzip The.Equalizer.srt` | باز کردن فایل فشرده شده با gzip |
| `bunzip2 The.Equalizer.srt` | باز کردن فایل فشرده شده با bzip2 |

**Archiving:**

| Command | Description |
|---------|-------------|
| `tar -cf myarchive.tar.gz /usr/share` | ساخت یک فایل آرشیو با نام myarchive.tar |
| `tar -xf myarchive.tar.gz` | استخراج محتوای یک فایل آرشیو |
| `tar -z myarchive.tar.gz` | فشرده سازی آرشیو با gzip بعد از ساخت |
| `tar -b myarchive.tar.gz` | فشرده سازی آرشیو با bzip2 بعد از ساخت |
| `tar -v myarchive.tar.gz` | نمایش جزئیات کامل عملیات در حال انجام (verbose) |
| `tar -r myarchive.tar.gz` | اضافه کردن فایل های جدید به آرشیو موجود |
| `tar -rf myarchive.tar.gz jadid` | فایل جدید را به آرشیو اضافه می کند |
| `dd if=/dev/zero of=1g.bin bs=1G count=1` | یک فایل با حجم مشخص میسازد |

---

## 103.4 — Use streams, pipes and redirects

| Command | Description |
|---------|-------------|
| `ls j* m* > output 2> errors` | خروجی استاندارد را در فایل خروجی ریخته و خروجی های دارای خطا را در فایل خطا میریزد |
| `ls j* m* >> output` | بدون overwrite |
| `ls j* &>` | خروجی استاندارد و خطا را با هم به یک مقصد هدایت میکند |
| `ls j* m* 1> output 2> &1` | بریز در همان جایی که خروجی استاندارد را ریختی — این کار از تکرار اسم فایل خروجی جلوگیری میکند |
| `tr ' ' ',' < users` | فایل یوزرها به عنوان فایل ورودی دستور می باشند |

**here-documents:**

| Command | Description |
|---------|-------------|
| `tr ' ' '.' << END` | از کاربر ورودی می گیرد تا زمانی که کاربر کلمه پایان را تایپ کند و بعد دستور را اجرا میکند |

**Pipes:**

| Command | Description |
|---------|-------------|
| `cut -f1 -d' ' what_i_have.txt \| sort \| uniq -c \| sort -nr` | پایپ تمام خروجی های دستور اول را به ورودی دستور دوم می دهد |

**xargs:**

| Command | Description |
|---------|-------------|
| `cat what_i_have.txt \| xargs -I DATA echo I have DATA and I love it` | این دستور ورودی میگیرد و جلو دستوری که جلو آن قرار دارد می گذارد |

**tee:**

| Command | Description |
|---------|-------------|
| `ls -1 \| tee allfiles myfiles` | لیست را در فایل میریزد و هم زمان نمایش هم میدهد |

---

## 103.5 — Create, monitor and kill processes

| Command | Description |
|---------|-------------|
| `xeyes &` | اجرای xeyes در پس زمینه |
| `Ctrl+z` | متوقف کردن پروسس و ارسال آن به پس زمینه |
| `jobs` | نمایش تمام دستورات در این ترمینال |
| `jobs -l` | نمایش لیست جاب ها به همراه شناسه پروسس (PID) |
| `bg %<proc number in jobs>` | برای ارسال یک دستور به بک گراند — این دستور یک پراسس را از حالت فریز نیز در می آورد |
| `fg %<proc number in jobs>` | برای ارسال یک دستور از بک گراند به فورگراند |
| `nohup sleep 1000 &` | دستور اسلیپ در کل سیستم اجرا شده و با بسته شدن ترمینال این دستور اجرا می گردد |

**kill:**

| Command | Description |
|---------|-------------|
| `kill %<proc number in jobs>` | پایان دادن به یک پروسس با استفاده از شماره جاب |
| `kill -9 <pid>` | در حالت عادی -15 میدهیم و در حالت بستن سریع -9 را میدهیم |
| `killall sleep` | تمام دستوراتی که در آن اسلیپ هست را می بندد |

**Processes:**

| Command | Description |
|---------|-------------|
| `ps` | تمامی پراسس های این ترمینال را نمایش میدهد |
| `ps -aux` | تمامی پراسس های سیستم را میدهد |
| `ps -ef` | همانند دستور قبلی می باشد با کمی تفاوت |
| `ps -lf` | همه پراسس های این ترمینال را با کمی جزئیات نمایش میدهد |
| `pstree` | نمایش درختی تمام پروسس های سیستم |

**top switches:**

| Key | Description |
|-----|-------------|
| `h` | نمایش راهنما |
| `q` | خروج از top |
| `M` | مرتب سازی بر اساس میزان مصرف حافظه |
| `c` | نمایش دستور کامل هر پروسس |
| `k` | پایان دادن به پروسس با پرسیدن PID و سیگنال |

**free:**

| Command | Description |
|---------|-------------|
| `free -m` | وضعیت رم را میدهد |
| `free -g` | نمایش وضعیت رم بر حسب گیگابایت |
| `uptime` | نمایش مدت زمان روشن بودن سیستم و بار پردازشی |

---

## 103.6 — Modify process execution priorities

| Command | Description |
|---------|-------------|
| `top` | برای دیدن اولویت پراسس های سیستم |
| `nice sleep 200 &` | اجرای دستور با اولویت پیش فرض (NI=0 تا NI=10) |
| `nice -n -20 sleep 200 &` | تعیین میزان اولویت |
| `ps -lf` | با این دستور مقدار اولویت هر دستور را در همان ترمینال میبینم |
| `renice -n -10 <procId>` | تغییر میزان اولویت |

---

## 103.7 — Search text files using regular expressions

| Command | Description |
|---------|-------------|
| `grep p friends` | جستجو هر چیزی که در آن p دارد |
| `grep p *` | هر فایلی که در همین دایرکتوری جاری دارای p باشد |
| `egrep "a+" friends.txt` | حتما یکی داشته باشد |
| `egrep "a*" friends.txt` | میتواند صفر یا بیشتر داشته باشد |
| `egrep "a?" friends.txt` | یا یکی یا هیچی |
| `egrep "^a" friends.txt` | با این کاراکتر شروع شود |
| `egrep "a$" friends.txt` | با این کاراکتر تمام شود |
| `egrep "a{2,4}" friends.txt` | حداقل دوتا و حداکثر چهارتا |
| `egrep "^(a\|b)" friends.txt` | با آ یا بی شروع گردد |
| `egrep -c a friends.txt` | تعداد را میدهد |
| `egrep -v a friends.txt` | آن هایی که این کاراکتر را ندارند را نمایش میدهد |
| `egrep -n a friends.txt` | شماره خط آن هایی که این کاراکتر را دارند را نمایش میدهد |
| `egrep -l a *` | لیست فایل هایی که در این دایرکتوری این کاراکتر را دارند را نمایش میدهد |
| `egrep -i a friends.txt` | نسبت به حروف بزرگ و کوچک بی تاثیر میکند |
| `fgrep "d$" friends.txt` | دقیقا همان عبارتی که جلو آن میگذاریم را جستجو میکند و عبارت های خاص را بی تاثیر میکند |

**Character classes:**

| Class | Description |
|-------|-------------|
| `[:alnum:]` | تمام حروف بزرگ و کوچک و اعداد |
| `[:blank:]` | فاصله (space) و تب (tab) |
| `[:digit:]` | اعداد ۰ تا ۹ |

**Regular expression metacharacters:**

| Metacharacter | Description |
|---------------|-------------|
| `.` | با هر کاراکتر منفردی تطابق پیدا میکند |
| `?` | آیتم قبلی اختیاری است و حداکثر یک بار تطابق پیدا میکند |
| `*` | آیتم قبلی صفر بار یا بیشتر تطابق پیدا میکند |
| `+` | آیتم قبلی یک بار یا بیشتر تطابق پیدا میکند |
| `{N}` | آیتم قبلی دقیقاً N بار تطابق پیدا میکند |
| `{N,}` | آیتم قبلی N بار یا بیشتر تطابق پیدا میکند |
| `{N,M}` | آیتم قبلی حداقل N بار و حداکثر M بار تطابق پیدا میکند |
| `-` | نمایانگر یک بازه در صورتی که اول یا آخر لیست نباشد |
| `^` | تطابق با رشته خالی در ابتدای خط؛ یا نفی کاراکترهای داخل براکت |
| `$` | تطابق با رشته خالی در انتهای خط |
| `\b` | تطابق با رشته خالی در مرز کلمه |
| `\B` | تطابق با رشته خالی در جایی که مرز کلمه نباشد |
| `\<` | تطابق با رشته خالی در ابتدای کلمه |
| `\>` | تطابق با رشته خالی در انتهای کلمه |

---

## 103.8 — Perform basic file editing operations using vi

```
vi file.txt
```

**Moving the cursor:**

| Key | Description |
|-----|-------------|
| `w` | رفتن به کلمه بعدی در خط جاری |
| `b` | رفتن به ابتدای کلمه قبلی در خط جاری |
| `e` | رفتن به انتهای کلمه بعدی در خط جاری |
| `Ctrl-f` | اسکرول به جلو یک صفحه |
| `Ctrl-b` | اسکرول به عقب یک صفحه |

**Jumping:**

| Key | Description |
|-----|-------------|
| `3G` | بدون عدد به انتهای فایل میرود؛ با عدد به آن خط میرود (مثلاً 10G به خط ۱۰) |
| `5L` | رفتن به xامین خط از انتهای صفحه (مثلاً 3L به سومین خط از آخر صفحه) |
| `3H` | رفتن به xامین خط از بالای صفحه (مثلاً 5H به پنجمین خط از بالا) |

**Editing text:**

| Key | Description |
|-----|-------------|
| `i` | ورود به حالت insert قبل از موقعیت فعلی مکان نما |
| `a` | ورود به حالت insert بعد از موقعیت فعلی مکان نما |
| `r` | جایگزین کردن فقط یک کاراکتر |
| `o` | ایجاد خط جدید زیر مکان نما و ورود به حالت insert |
| `O` | ایجاد خط جدید بالای مکان نما و ورود به حالت insert |
| `c` | پاک کردن تا یک موقعیت و ورود به حالت insert برای جایگزینی (cw کلمه جاری را جایگزین میکند) |

**Delete:**

| Key | Description |
|-----|-------------|
| `dw` | حذف کلمه جاری |
| `d$` | حذف از موقعیت جاری تا انتهای خط |
| `d^` | حذف از موقعیت جاری تا ابتدای خط |
| `dd` | حذف خط جاری |
| `6dd` | حذف ۶ خط |
| `x` | حذف کاراکتر زیر مکان نما |
| `p` | الصاق آخرین متن حذف شده بعد از مکان نما |
| `P` | الصاق آخرین متن حذف شده قبل از مکان نما |
| `xp` | جابجایی کاراکتر زیر مکان نما با کاراکتر سمت راست آن |

**Replace:**

```
c --> (destination) --> type replace content --> escape
example: c --> $ or ^ or b --> hiiiiiii --> escape
```

**Searching:**

| Key | Description |
|-----|-------------|
| `/` | جستجوی رو به جلو در فایل |
| `?` | جستجوی رو به عقب در فایل |
| `n` | تکرار جستجوی قبلی |

**Exiting:**

| Key | Description |
|-----|-------------|
| `:q!` | خروج بدون ذخیره — فرار از هر اشتباهی |
| `:w!` | ذخیره فایل (چه تغییر کرده باشد چه نه)؛ سعی میکند فایل های فقط-خواندنی را هم بنویسد |
| `:w myfile.txt` | ذخیره با نام جدید |
| `ZZ` | خروج و ذخیره در صورت تغییر فایل |
| `:e!` | بارگذاری مجدد فایل از دیسک بدون ذخیره تغییرات |
| `:!` | اجرای یک دستور شل بدون خروج از vi |
| `:!ls` | اجرای دستور ls و بازگشت به vi |

---

## 104.1 — Create partitions and filesystems

| Command | Description |
|---------|-------------|
| `ls -l /dev/sd[a-z]` | نمایش لیست دیسک های سیستم |
| `fdisk -l /dev/sda` | نمایش لیست پارتیشن های یک دیسک |
| `fdisk /dev/sda` | ورود به محیط fdisk |

**fdisk switches:**

| Key | Description |
|-----|-------------|
| `m` | نمایش راهنما |
| `p` | نمایش لیست پارتیشن ها |
| `l` | نمایش انواع پارتیشن به همراه شناسه های آن ها |
| `d` | حذف یک پارتیشن |
| `n` | ایجاد پارتیشن جدید |
| `t` | تغییر نوع پارتیشن |
| `v` | بررسی صحت جدول پارتیشن بندی |
| `w` | نوشتن تغییرات و خروج |
| `q` | خروج بدون ذخیره تغییرات |

**Partition Format:**

```bash
mkfs -t ext3 -L mohammad /dev/sda1
```

**Create swap:**

```bash
mkswap /dev/sda4
```

| Command | Description |
|---------|-------------|
| `hwinfo --block --short` | نمایش خلاصه اطلاعات دستگاه های بلاک (دیسک ها) |
| `hwinfo` | نمایش تمام جزئیات سخت افزاری سیستم |

---

## 104.2 — Maintain the integrity of filesystems

| Command | Description |
|---------|-------------|
| `fsck /dev/sdb` | بررسی و تعمیر فایل سیستم یک پارتیشن |
| `blkid` | گرفتن اطلاعات هاردها |

**df:**

| Command | Description |
|---------|-------------|
| `df -h` | اطلاعات پارتیشن ها بر اساس 1000 بایت |
| `df -H` | اطلاعات پارتیشن ها بر اساس 1024 بایت |
| `df -TH` | اطلاعات پارتیشن ها با نوع تایپ آن ها |
| `df -ih` | نمایش اطلاعات نود ها |

**du:**

| Command | Description |
|---------|-------------|
| `du` | نمایش حجم دایرکتوری جاری |
| `du -h -c /run/media/mohammad` | میزان سایز یک آدرس را به ما نمایش میدهد و در خط آخر حجم کل را نمایش میدهد |
| `du -hs` | دقیقا سایز همان دایرکتوری را میدهد |

| Command | Description |
|---------|-------------|
| `debugfs /dev/sda2` | ابزار دیباگ فایل سیستم ext برای بررسی و تعمیر |
| `mke2fs -n /dev/sda7` | نمایش آدرس سوپر بلاک های یک پارتیشن |

---

## 104.3 — Control mounting and unmounting of filesystems

| Command | Description |
|---------|-------------|
| `cat /etc/fstab` | تمامی پارتیشن های مانت شده را نمایش میدهد |
| `mount` | تمام پارتیشن های مانت شده را نمایش میدهد |
| `mount /dev/sda1 /media` | مانت کردن پارتیشن sda1 روی دایرکتوری media/ |
| `umount /media` | آنمانت کردن پارتیشن از دایرکتوری media/ |
| `mount -o remount,ro /dev/sda1 /media` | مانت مجدد پارتیشن با گزینه فقط خواندنی (ro=فقط خواندنی، rw=خواندن و نوشتن) |
| `mount -t ext4 /dev/sda1 /media` | فرمت فایل سیستم من این است و اگر نگذاریم خودش میفهمد |

**swap:**

| Command | Description |
|---------|-------------|
| `swapon` | فعال کردن فضای swap |
| `swapoff` | غیرفعال کردن فضای swap |
| `swapon -s` | نمایش وضعیت فعلی swap |

برای اینکه یک پارتیشن را یک یوزر معمولی بتواند به صورت خودکار مانت کند خط زیر را در فایل زیر اضافه میکنیم:

```bash
vi /etc/fstab
/dev/sdaX      none            swap      sw         0        0
```

---

## 104.4 — Manage disk quotas

| Command | Description |
|---------|-------------|
| `/dev/sda2 /home ext4 defaults,usrquota,grpquota` | نحوه مقدار دهی در فایل fstab |
| `quotacheck -u -a -m -c -v` | برای چک کردن فضای هر یوزر (`u`=user, `a`=all, `m`=mount) |
| `quotaon /dev/sda1` | فعال کردن quota روی یک پارتیشن |
| `quotaoff /dev/sda1` | غیرفعال کردن quota روی یک پارتیشن |
| `quotaon -auv` | خواندن فایل fstab و فعال کردن usrquota برای همه پارتیشن ها |
| `edquota -u mohammad` | برای ادیت یک کاربر |
| `quota mohammad` | برای مشاهده وضعیت یک کاربر |
| `repquota -u -a` | برای گزارش گیری از وضعیت تمامی یوزرها |

---

## 104.5 — Manage file permissions and ownership

| Command | Description |
|---------|-------------|
| `whoami` | نمایش نام کاربر فعلی |
| `groups` | گروه هایی که این کاربر در آن عضو هستند را نمایش میدهد |
| `id` | آی دی یوزرها و گروه ها را نمایش میدهد |
| `cat /etc/group` | همه گروه ها اینجا هستند |
| `cat /etc/passwd` | همه یوزرها اینجا هستند |
| `ls -l /lpic/notes.txt` | نمایش وضعیت دسترسی های هر فایل |
| `chmod (u,g,o)+(r,w,x) test.txt` | تغییر دسترسی به هر فایل |
| `chmod 751 myfile` | همانند فایل بالا |
| `chmod u+s` | suid — هر کس این فایل را اجرا کند با دسترسی سازنده فایل خواهد بود |
| `chmod g+s` | guid — همانند بالا فقط برای گروه ها |
| `chmod o+s` | sticky bit — فقط مالک فایل میتواند آن را حذف کند |
| `umask` | چه دسترسی هایی نباید به یک فایل بدهیم |
| `chown root:root test.txt` | برای تغییر صاحب یک فایل |

**ls -ltrh output format:**

```
drwxr-xr-x.   3   root   root   4.0K   Jun 17 10:43   java.txt
permissions   num_subfiles   user   group   size   date   filename
```

---

## 104.6 — Create and change hard & symbolic links

| Command | Description |
|---------|-------------|
| `ln myfile.txt hardlink.txt` | ساخت یک هارد لینک — هر دو فایل به یک inode اشاره میکنند |
| `ln -s myfile.txt softlink` | ساخت یک لینک نمادین (سافت لینک) |
| `ln -s mydir link2dir` | لینک کردن دایرکتوری ها |
| `find . -type l` | برای پیدا کردن تمامی لینک ها در دایرکتوری فعلی |

---

## 104.7 — Find system files and place files in the correct location

| Command | Description |
|---------|-------------|
| `which mkfd` | نمایش مسیر کامل یک دستور |
| `type for` | نمایش نوع یک دستور (builtin، alias، فایل اجرایی) |
| `whereis ping` | سه دستور بالا آدرس ها و محل هایی که این دستورات در آن ها قرار دارند را نمایش میدهد |
| `find /tmp/ -maxdepth 1 -user mohammad` | هر فایلی در تمپ که برای یوزر جادی هست را میدهد |
| `locate happy` | دستور خیلی بهتر است برای جستجو هر فایلی که در آن اسم آن هپی هست |
| `locate -S` | نمایش اطلاعات و مکان پایگاه داده آفلاین دستور locate |

---

## 105.1 — Customize and use the shell environment

| Command | Description |
|---------|-------------|
| `/etc/profile` | محل قرار گیری path |
| `/etc/profile.d/*` | فایل هایی که میخواهیم در شل و در همه یوزرها اجرا شوند را در این دایرکتوری قرار میدهیم |
| `alias ll='ls -alF'` | تعریف یک نام مستعار (alias) برای یک دستور |

**Function example:**

```bash
funnyls () {
    ls -ltrh
    echo "This is a funny ls"
}
```

**set switches:**

| Command | Description |
|---------|-------------|
| `set -b` | بصورت همزمان موقع بک را نمایش میدهد |
| `set -e` | اگر خروجی دستور صفر بود یعنی دستورات بدون خطا انجام شده اند در غیر اینصورت خطا داریم |
| `set -n` | دستور را میخواند ولی اجرا نمیکند |
| `set -t` | بعد از اجرا دستورات خارج میشود |
| `sleep 5 & set -b` | مثال استفاده از set -b برای نمایش فوری وضعیت پس‌زمینه |

| Command | Description |
|---------|-------------|
| `export name=mohammad` | دسترسی به این متغیر در تمام پارسس های فرزندان این بش |
| `unset funnyls` | این دستور وظیفه دارد متغیر های محلی را از بین ببرد |
| `env name="mohammad"` | این دستور همه متغیر های محلی را نمایش میدهد و در آخر جاری را |

**Arrays:**

| Command | Description |
|---------|-------------|
| `list=(salam donya man injam)` | تعریف یک لیست |
| `echo ${list[1]}` | یک همان دنیا است دو همان من و ... |

---

## 105.2 — Customize or write simple scripts

```bash
FILES=$(ls -1)   # هر چه بین دو پرانتز باشد آن را در آن متغیر میریزد
```

**if statement:**

```bash
#!/bin/bash
if [ condition ]
then
    do something
    do another thing
else
    do new things
    even funnier things
fi
```

**if conditions:**

| Condition | Description |
|-----------|-------------|
| `"a" = "b"` | اگر دو رشته برابر باشند (اینجا False برمیگرداند) |
| `"a" != "b"` | اگر رشته a با رشته b برابر نباشد |
| `4 -lt 40` | اگر ۴ کمتر از ۴۰ باشد (True) |
| `5 -gt 15` | اگر ۵ بزرگتر از ۱۵ باشد (False) |
| `5 -ge 5` | اگر ۵ بزرگتر یا مساوی ۵ باشد |
| `5 -le 3` | اگر ۵ کوچکتر یا مساوی ۳ باشد |
| `9 -ne 2` | اگر ۹ با ۲ برابر نباشد (True) |
| `-f FILENAME` | اگر فایل FILENAME وجود داشته باشد |
| `-s FILENAME` | اگر فایل وجود داشته باشد و سایز آن بیشتر از صفر باشد |
| `-x FILENAME` | اگر فایل وجود داشته باشد و قابل اجرا باشد |

**read:**

```bash
#!/bin/sh
echo "what is your name?"
read NAME
echo "Hello $NAME"   # رید یک مقداری از کامند لاین میخواند
```

**for loop:**

```bash
for FILE in $(ls);
do
    echo $FILE
    wc $FILE
done
```

**while loop:**

```bash
VAR=52
while [ $VAR -gt 42 ]
do
    echo VAR is $VAR and it is still greater than 42
    let VAR=VAR-1
done
```

**mailing:**

```bash
mohammad@funlife:~$ mail root
Cc:
Subject: Hi there root
hello there. This is my mail
```

---

## 105.3 — SQL data management

| Command | Description |
|---------|-------------|
| `mysql -u root -p` | ورود به دیتابیس |
| `SHOW DATABASES;` | حتما آخر دستورات `;` را بگذارید |
| `USE LPIC;` | انتخاب جدول |
| `SHOW TABLES;` | نمایش جداول |
| `SELECT * FROM phonebook;` | نمایش تمام رکوردهای جدول phonebook |
| `SELECT name FROM phonebook;` | نمایش فقط ستون name از جدول phonebook |
| `SELECT * FROM info WHERE mood = 'happy';` | نمایش رکوردهایی که مقدار mood برابر happy است |
| `SELECT * FROM info WHERE mood = 'happy' AND weight >= 80;` | فیلتر با دو شرط همزمان |
| `SELECT * FROM phonebook ORDER BY name;` | نمایش رکوردها مرتب شده بر اساس نام |
| `SELECT * FROM info GROUP BY mood;` | گروه بندی رکوردها بر اساس mood |
| `INSERT INTO phonebook (name, phone, email) VALUES ('ghasem', '+982112345678','');` | اضافه کردن یک رکورد جدید به جدول |
| `UPDATE phonebook SET email='haale@lpic.fake' WHERE name = 'haale';` | به روزرسانی ایمیل رکوردی که نام آن haale است |
| `SELECT * FROM phonebook JOIN info;` | ترکیب داده های دو جدول با join |

---

## 106.1 — Install and configure X11

> This content is very old and commands don't work in new versions of Linux distributions.

| Command | Description |
|---------|-------------|
| `/etc/X11/xorg.conf` | محل قرارگیری کانفیگ های محیط X |
| `xwininfo` | اطلاعات یک پنجره در محیط X |
| `xdpyinfo` | اطلاعات خود display |
| `xhost` | چه کسانی به ایکس این کامپیوتر دسترسی دارند |
| `xhost +` | ایکس برای همه باز شود |
| `xhost -` | ایکس برای همه بسته شود |
| `echo $DISPLAY` | شماره دیسپلی را نمایش میدهد |
| `export DISPLAY=192.168.42.85:0` | محیط گرافیکی من را در این آدرس نمایش بده |

---

## 106.2 — Setup a display manager

| Command / Path | Description |
|----------------|-------------|
| `lightdm` | سرویس مدیریت نمایش (Display Manager) لینوکس |
| `/etc/lightdm/` | دایرکتوری فایل های کانفیگ lightdm |
| `greeter-session=lightdm-webkit2-greeter` | این قسمت از فایل بالا نام تم انتخاب شده را نمایش میدهد |

---

## 106.3 — Accessibility

> This chapter doesn't have any commands.

---

## 107.1 — Manage user and group accounts

| Command | Description |
|---------|-------------|
| `passwd` | تغییر پسورد |
| `passwd mohammad` | تغییر پسورد یک کاربر توسط یوزر روت |

**useradd:**

| Command | Description |
|---------|-------------|
| `useradd mohammad` | ساخت یک کاربر جدید با تنظیمات پیش فرض |
| `useradd -d /.../... mohammad` | تعیین دایرکتوری خانگی برای کاربر |
| `useradd -m /.../... mohammad` | ساخت و تعیین دایرکتوری خانگی برای کاربر |
| `useradd -s /bin/bzr mohammad` | یوزر در چه برنامه ای لاگین شود |
| `useradd -G wheel mohammad` | یوزر را عضو یک گروه میکنیم |
| `useradd -c 'mohammad khalatbari' mohammad` | یک نام کامل به کاربر میدهیم |

**Modifying User:**

| Command | Description |
|---------|-------------|
| `usermod -c 'mohammad azizi' mohammad` | تغییر نام کامل (comment) کاربر |
| `usermod -s ...` | تغییر شل پیش فرض کاربر |
| `usermod -aG wheel mohammad` | یوزر را به یک گروه وارد میکنیم با این تفاوت که گروه های قبلی حذف نمی گردند |
| `useradd -L mohammad` | لاک کردن یک یوزر |
| `useradd -U mohammad` | خروج یک یوزر از حالت لاک |

**Delete User:**

| Command | Description |
|---------|-------------|
| `userdel mohammad` | حذف کاربر |
| `userdel -r mohammad` | حذف کاربر به همراه حذف home directory |

**Managing Groups:**

| Command | Description |
|---------|-------------|
| `groupadd managers` | ساخت یک گروه جدید |
| `groupdel managers` | حذف یک گروه |
| `groupadd -g 2222 managers` | تخصیص یک شماره به یک گروه |
| `groupmod -g 2222 managers` | تغییر شناسه عددی (GID) یک گروه موجود |

**User info:**

| Command | Description |
|---------|-------------|
| `/etc/passwd` | نمایش اطلاعات کاربران |
| `/etc/shadow` | محل قرار گیری پسورد به همراه اطلاعات دیگر |
| `chage -l mohammad` | برای بهتر خواندن اطلاعات shadow از این دستور استفاده میکنیم |
| `chage mohammad` | تنظیم اطلاعاتی که در دستور بالا دیدیم |
| `chage -E mohammad` | مشخص کردن تاریخ انقضا رمز عبور |
| `/etc/group` | نمایش اطلاعات مربوط به گروه ها |
| `id mohammad` | نمایش UID، GID و گروه های کاربر |
| `getent group wheel` | نمایش اطلاعات یک گروه از پایگاه داده سیستم |
| `getent passwd mohammad` | سه دستور بالا اطلاعاتی در مورد هر کاربر به ما میدهد |
| `usermod -s /bin/nologin mohammad` | یوزر لاک نیست ولی لاگین هم نمیتواند بکند |

---

## 107.2 — Automate system administration tasks by scheduling jobs

| Command | Description |
|---------|-------------|
| `crontab -l` | لیست کارهایی که برای این کاربر ست شده است را نمایش میدهد |
| `crontab -e` | برای اضافه کردن یک کار موارد زیر را به انتهای این فایل اضافه میکنیم |

**Crontab format:**

```
m   h   dom   mon   dow   command
```
> دقیقه — ساعت — روز ماه — ماه — روز هفته — دستور

```bash
5 1 * * * $HOME/bin/daily.job >> $HOME/tmp/out 2>&1
# دقیقه پنجم ساعت یک هر روز از هر ماه و هر روز هفته
```

**AT:**

| Command | Description |
|---------|-------------|
| `at now +2 min` | از الان تا دو دقیقه بعد این دستورات را انجام بده |
| `at tomorrow` | اجرای دستوراتی که وارد میشوند در فردا |
| `at 08:00` | اجرای دستوراتی که وارد میشوند در ساعت ۸ صبح |
| `atq` | کارهایی را که در حال انجام است را نمایش میدهد |
| `atrm` | پاک کردن یک کار |

**System Wide cron:**

```bash
*/15 * * * * root test -x /usr/lib/cron/run-crons && /usr/lib/cron/run-crons >/dev/null 2>&1
```

**Access control files:**

| File | Description |
|------|-------------|
| `/etc/cron.allow` | لیست کاربرانی که مجاز به استفاده از cron هستند |
| `/etc/cron.deny` | لیست کاربرانی که از استفاده از cron محروم هستند |
| `/etc/at.allow` | لیست کاربرانی که مجاز به استفاده از at هستند |
| `/etc/at.deny` | چهار فایل بالا برای دسترسی به یوزرها هستند و فقط کافیست نام یوزر را در آن ها بنویسیم |

---

## 107.3 — Localisation and internationalisation

| Command | Description |
|---------|-------------|
| `date +'%Y%m%d-%H%M'` | نمایش تاریخ به فرمت دلخواه ما |
| `tzselect` | تنظیم timezone |
| `TZ='Asia/Tehran'; export TZ` | تنظیم timezone |
| `locale` | برخی متغیر های محلی که مربوط به زبان سیستم هست را نمایش میدهد |
| `export LC_ALL=fa_IR.UTF-8` | برای تغییر استاندارد زبان سیستم |
| `export LC_ALL=C` | در این حالت source older براساس binary میباشد |
| `iconv -f WINDOWS-1258 -t UTF-8 /tmp/myfile.txt` | تغییر فرمت سمت چپ به فرمت سمت راست |

---

## 108.1 — Maintain system time

| Command | Description |
|---------|-------------|
| `cat /etc/adjtime` | نمایش اطلاعات انحراف ساعت سخت افزار از ساعت واقعی |
| `date` | ساعت و تاریخ سیستم |
| `hwclock` | ساعت سخت افزار |
| `hwclock --localtime --set --date="01/05/2015 22:04:00"` | ساعت سخت افزار بر اساس ساعت لوکال |
| `hwclock -u -w` | ساعت سخت افزار بر اساس universal |
| `ntpdate pool.ntp.org` | از سرور ntp ساعت را میپرسد |
| `hwclock -w` | همان مقدار دستور بالا را روی ساعت سخت افزاری مینویسد |
| `apt install ntp` | نصب سرویس ntp |
| `systemctl start ntp` | راه اندازی سرویس ntp |
| `systemctl enable ntp` | هر سه دستور بالا برای نصب و راه اندازی سرویس ntp می باشد |
| `systemctl status ntp` | مشاهده وضعیت سرویس ntp |
| `ntpdate pool.ntp.org` | همگام سازی دستی ساعت با سرور ntp |
| `ntpq -p` | یک کوئری به سرور ان تی پی میزند و بعد مقدار انتخاب شده توسط سیستم ما را نیز نمایش میدهد |

---

## 108.2 — System logging

| Command | Description |
|---------|-------------|
| `less /etc/syslog.conf` | در این فایل برخی خط ها وجود دارد که مشخص میکند هر نوع خطا را باید چه اکشنی انجام دهد |
| `user.*   -/var/log/user.log` | یکی از خط های همان فایل است که میگوید هر کاری که کاربر انجام داد را در آن فایل ثبت کن |

```bash
vi /etc/default/rsyslog
    RSYSLOG_PRODILE="-r"   # creating rsyslog listener
systemctl restart rsyslog
```

| Command | Description |
|---------|-------------|
| `journalctl` | مشاهده تمام لاگ های ثبت شده توسط systemd |
| `logger local1.info mohammad was here` | ثبت یک لاگ در سیستم |
| `tail /var/log/syslog` | مشاهده لاگ بالا |

**logrotate:**

| Config / Command | Description |
|------------------|-------------|
| `cd /etc/logrotate.d` | دایرکتوری تنظیمات logrotate برای هر سرویس |
| `cat /etc/logrotate.conf` | مشاهده فایل کانفیگ اصلی logrotate |
| `weekly` | هفته ای یکبار فایل جدید برای لاگ درست کرده و فایل قدیمی را به تاریخ آن روز تغییر بده |
| `rotate 52` | فقط ۵۲ فایل آخر را نگه دار و فایل قدیمی تر را پاک کن |
| `missingok` | اگر لاگ نداشت مشکلی نیست |
| `compress` | فشرده سازی هم انجام بده |
| `create 0640 www-data adm` | فایل هایی با این دسترسی بساز |

---

## 108.3 — Mail Transfer Agent (MTA) basics

| Command | Description |
|---------|-------------|
| `cat /etc/aliases` | این فایل حاوی دریافت گیرندگان ایمیل هاست |
| `root: mohammad` | هر ایمیلی برای روت آمد را بفرست برای محمد |
| `newaliases` | اگر یک مقدار جدید در فایل بالا نوشتیم این دستور را میزنیم تا اجرا گردد |
| `mail mohammad` | ارسال یک ایمیل به محمد |
| `mail` | نمایش ایمیل های هر کاربر |

**local forward:**

| Command | Description |
|---------|-------------|
| `vi .forward` | ساخت یک لوکال فوروارد که این برای کاربران معمولی می باشد |
| `mohammad@gmail.com` | همه ایمیل هایی که این کاربر دریافت میکند را به این آدرس فوروارد می کند |
| `mailq` | صف ایمیل ها را نمایش میدهد |

---

## 108.4 — Manage printers and printing

| Command | Description |
|---------|-------------|
| `cups` | سرویس چاپ یونیکس (Common Unix Printing Service) |
| `localhost:631` | آدرس وب رابط مدیریت cups |
| `/etc/cups/cups.conf` | فایل کانفیگ cups |
| `/etc/cups/printers.conf` | تنظیمات پرینترهای نصب شده اینجا قرار دارد |
| `lpr test.txt` | چاپ یک فایل روی پرینتر پیش فرض |
| `lpr -Pmy_printer test.txt` | چاپ یک فایل روی پرینتر انتخابی |
| `lpq test.txt` | نمایش صف چاپ و وضعیت کارها برای پرینتر پیش فرض |
| `lpq -a` | نمایش صف چاپ برای تمام پرینترها |
| `lprm <job id>` | حذف یک کار از صف پرینتر |
| `lprm -Pmy_printer` | حذف تمام کارها از صف یک پرینتر خاص |
| `lpc test.txt` | برنامه کنترل و عیب یابی پرینتر و بررسی وضعیت آن |
| `cupsaccept my_printer` | فعال کردن دریافت کارهای جدید در صف پرینتر |
| `cupsreject my_printer` | غیرفعال کردن دریافت کارهای جدید در صف پرینتر |
| `cupsenable my_printer` | فعال کردن چاپ فیزیکی واقعی کارها |
| `cupsdisable my_printer` | غیرفعال کردن چاپ فیزیکی (کارها دریافت میشوند ولی چاپ نمیشوند) |

---

## 109.1 — Fundamentals of internet protocols

> This chapter speaks about basic information of networking.

**Important ports:**

| Port | Protocol |
|------|----------|
| `20, 21` | FTP — انتقال فایل (یک کانال داده، یک کانال کنترل) |
| `22` | SSH — اتصال امن از راه دور |
| `23` | Telnet — اتصال از راه دور بدون رمزنگاری |
| `25` | SMTP — ارسال ایمیل |
| `53` | DNS — سرویس نام دامنه |
| `80` | HTTP — وب سایت های بدون رمزنگاری |
| `110` | POP3 — دریافت ایمیل |
| `123` | NTP — هماهنگ سازی ساعت شبکه |
| `139` | NetBIOS — اشتراک گذاری فایل ویندوز |
| `143` | IMAP — دسترسی به ایمیل روی سرور |
| `161, 162` | SNMP — مدیریت و پایش شبکه |
| `389` | LDAP — سرویس دایرکتوری |
| `443` | HTTPS — وب سایت های رمزنگاری شده |
| `465` | SMTPS — ارسال ایمیل رمزنگاری شده |
| `636` | LDAPS — سرویس دایرکتوری رمزنگاری شده |
| `993` | IMAPS — دسترسی ایمن به ایمیل روی سرور |
| `995` | POP3S — دریافت ایمیل رمزنگاری شده |

---

## 109.2 — Basic network configuration

| Command | Description |
|---------|-------------|
| `ifconfig` | لیست کارت شبکه های فعال |
| `ifconfig -a` | لیست تمامی کارت شبکه ها (فعال و غیر فعال) |
| `ifconfig eth0 192.168.42.42 netmask 255.255.255.0` | تنظیم یک آی پی آدرس روی یک کارت شبکه |
| `ifconfig enp0s25 down` | غیر فعال کردن کارت شبکه |
| `ifconfig enp0s25 up` | فعال کردن کارت شبکه |
| `cat /etc/sysconfig/network-scripts/ifcfg-eth0` | نمایش اطلاعات مربوط به کارت شبکه و امکان تغییر تنظیمات آن ها |
| `cat /etc/resolv.conf` | میتوانیم دی ان اس را هم در اینجا و هم در فایل بالا تنظیم کنیم |
| `cat /etc/hostname` | نمایش نام هاست سیستم |
| `cat /etc/hosts` | همانند یک دی ان اس لوکال می باشد — همه هاست های سیستم مارا نشان میدهد |
| `route` | نمایش جدول مسیریابی شبکه |
| `netstat -nr` | همانند دستور بالا |
| `route add default gw 192.168.1.1` | یک روت اضافه کردیم |
| `ip addr show` | همانند دستور ifconfig |
| `cat /etc/nsswitch.conf` | ترتیب اولویت خواندن فایل ها را نمایش میدهد |
| `hosts: dns files` | برای مثال اینجا هاست ها اول دی ان اس را چک میکند و بعد فایل ها را |

---

## 109.3 — Basic network troubleshooting

> This chapter is about network troubleshooting and doesn't have any new commands.

---

## 109.4 — Configure client side DNS

> This chapter is about network troubleshooting and doesn't have any new commands.

---

## 110.1 — Perform security administration tasks

| Command | Description |
|---------|-------------|
| `find / -perm -u+s` | این دستوراتی که برای آن ها suid ثبت شد |
| `netstat -na \| grep listen` | پورت هایی در سیستم ما که در حال گوش دادن هستند |
| `netstat -tuna` | همانند دستور بالا بدون ذکر نام برنامه |
| `netstat -p` | همانند دستور بالا با ذکر نام برنامه |
| `lsof` | این دستور لیست تمام کانکشن های سیستم را میدهد |
| `lsof -i` | لیست تمام کانکشن های ارتباطی را میدهد |
| `fuser 80/tcp` | میگوید که روی این پورت چه پروسه هایی دارند کار میکنند |
| `nmap localhost` | اطلاعات سیستم خودمان را میدهد |
| `nmap microsoft.com` | اسکن پورت های یک هاست خارجی |
| `su` | نام هر یوزری که جلو آن بنویسیم پسورد آن یوزر را گرفته و به همان یوزر تبدیل می گردد |
| `su - mohammad` | تغییر به کاربر محمد به همراه بارگذاری محیط شل آن کاربر |
| `su -` | حالت پیش فرض است که وارد یوزر روت می شود |
| `sudo cat /etc/sudoers` | تمام دسترسی ها اینجا مشخص گردیده است — این فایل را نباید اصلا تغییر دهیم |
| `visudo` | برای تغییر در دسترسی های فایل بالا از این دستور استفاده میکنیم |
| `ulimit -a` | وضعیت دسترسی هر یوزر به برخی موارد سیستمی را نمایش میدهد |
| `ulimit -t 1` | برای تغییر میتوانیم همانند این دستور را بزنیم |
| `time cp ...` | این دستور زمان انجام هر دستور را نمایش میدهد |

**Checking users in the system:**

| Command | Description |
|---------|-------------|
| `w` | چه کسانی در سیستم هستند و چیکار میکنند |
| `who` | همان دستور بالا با اطلاعات کمتر |
| `last` | چه کسانی آخرین بار وارد سیستم شده اند |
| `last -f /var/log/btmp` | لاگین هایی که یوزرها سعی کردند انجام دهند ولی به خطا خوردند |

---

## 110.2 — Setup host security

| Command | Description |
|---------|-------------|
| `cat /etc/hosts.allow` | نمایش فایل تنظیمات سرویس هایی که مجاز به دسترسی هستند (TCP Wrappers) |
| `ftp: 10.10.10. localhost` | یعنی این سرویس میتواند از این دو آدرس استفاده کند |
| `vi /etc/nologin` | این فایل را می سازیم و هر یوزر که لاگین کرد محتوای این فایل را می بیند |
| `chkconfig httpd off` | غیرفعال کردن سرویس در سیستم sysV (روش قدیمی ردهت) |
| `sysv-rc-conf httpd off` | خاموش کردن سرویس ها در سیستم sysV |
| `update-rc.d httpd remove` | خاموش کردن سرویس در upstart |
| `systemctl disable httpd` | خاموش کردن سرویس در systemd |

---

## 110.3 — Securing data with encryption

| Command | Description |
|---------|-------------|
| `ssh-keygen` | ساخت جفت کلید عمومی و خصوصی SSH |
| `ssh-copy-id 10.0.2.15` | کلید پابلیک را روی مقصد میریزد |
| `ssh-agent` | وظیفه مدیریت کلیدها را بر عهده دارد |
| `ssh-add -l` | لیست کلیدها را نمایش میدهد |
| `ssh-add -D` | پاک کردن کلیدها |
| `ssh-add` | از روی فایل های ساخته شده دوباره کلیدها را می سازد |
| `/etc/ssh` | دایرکتوری فایل های کانفیگ سرویس SSH |
| `gpg --gen-key` | کلید را در سیستم خودمان میسازد |
| `cd .gnupg` | محل قرار گیری کلیدها |
| `gpg --export name > gpg.pub` | کلید را برای کسی ارسال میکنیم |
| `gpg --import gpg.pub` | وارد کردن یک کلید به سیستم خودمان |
| `gpg --out file.txt.encrypted --recipient a@gmail.com --encrypt file.txt` | دستور بالا برای رمزنگاری یک فایل ساخته شده بر اساس یکی از کلیدهای ساخته شده می باشد |
| `gpg --out out.txt --decrypt file.txt.encrypted` | دستور بالا برای باز کردن فایل رمزنگاری شده در مقصد می باشد |
| `gpg --output revoke.asc --gen-revoke a@gmail.com` | این دستور برای ساخت revoke |
| `gpg --clearsign originalfile` | امضا فایل ما را میسازد و در یک فایل با پسوند asc میریزد |
| `gpg --verify recievedfile` | برای چک کردن امضا می باشد |

---

*End of LPIC-1 Commands Reference*
