<div>
  <img src="https://zeus.descubrecomohacerlo.com/uploads/images/content/android-conexion-usb_3766.jpg" title="ADB" alt="ADB" width="80"
</div>
  
### ADB_HW
  ___

 1. Отобразить подключенный девайс в консоли.

 ```
  .\adb devices
  ```
 2. Вывести адрес приложения reminder в системе Android
	
  ```
  .\adb shell 'pm list packages -f' | findstr reminder
  ```
 3. Установить .apk файл приложения reminder на телефон с компьютера через  ADB
	
  ```
  .\adb install E:\QA\courses\ADB\app-debug.apk
  ```
 4. Сделать скриншот запущенного приложения reminder и скопировать на компьютер.

  ``` 
  .\adb screencap /внутренний общий накопитель/DCIM/Screenshots/reminder.png
	.\adb pull /внутренний общий накопитель/DCIM/Screenshots/reminder.png reminder.png
  ```
 5. Вывести в консоль логи приложения reminder
	
  ```
  .\adb logcat -d | findstr com.qrolic.reminderapp
  ```
 6. Скопировать логи приложения reminder на компьютер.
	
  ```
  .\adb logcat -d | findstr com.qrolic.reminderapp > reminder.log
  ```
 7. Удалить приложение reminder с телефона через ADB
	
  ```
  .\adb uninstall com.qrolic.reminderapp
  ```
