

>[!quote]- What is OTA :
>- اختصار ل over the air
>- التكنولوجيا دي بتستخدم ف تحديثات السوفتوير للمايكروكونترولر عن طريق بروتوكول تواصل بيبقي اونلاين من غير اتصال سلكي بالمايكروكونترولر
>- حاجة زي الموبايلات بالظبط, لما بيجيلك تحديث لحاجة معينة
>----
>- السوفتوير بيتنقل بايت ب بايت وبيبقي عبارة عن ال exe file 
>---
>- ![[Pasted image 20240703115653.png]]
>---
>>[!todo]- It has 3 challenges :
>>>[!caution]- Memory :
>>>- the software must be organized in the memory to avoid:
>>>	- overwriting
>>>	- storing in volatile memory
>>>	- incomplete downloading by interrupt(power loss or communication errors)
>>>- يجب الاحتفاظ بنسخة باك اب للنظام القديم عشان لو التحديث الجديد فيه مشاكل ف تقدر ترجع للقديم لحد م يظبطوا النسخة الجديدة
>>---
>>>[!caution]- Communication :
>>>- وظيفته انشاء الاتصال بين السيرفر و ال client عشان الداتا تتنقل من خلاله
>>>- يتأكد من المكان اللي الداتا هتوصله وتتثبت فيه ف الميموري, default path
>>>- وظيفة ال IOT
>>---
>>>[!caution]- Security :
>>>- يعملوا ديزاين للبروتوكول المستخدم لنقل البيانات (ت س ب مثلا)
>>>- مسئوليين عن تأمين السيرفر ومين يقدر يدخل عليه (authentication)
>>>- تأمين الداتا المنقولة (بطرق التشفير المختلفة)
>>>- السيرفر يبقي متصل دايما ولو في مشكلة يعرفوا (حاجة مشتركة بينهم وبين IOT)

---
---

>[!caution]- SSBL - second storage boot loader :
>- necessary when the primary boot loader does not support Over-the-Air (OTA) updates
>---
>- التحديث بينزل ويتثبت ف الفلاش ميموري ولما يتم التأكد منه ...
>- البوت لودر هينقل التحكم للنسخة الجديدة و يشغلها مع كل مرة ترستر الجهاز
>---
>- بيحسن الاداء والدقة عن طريق فحص  البرنامج والتأكد منه قبل التشغيل.
>---
>>[!todo]- Problem solved :
>>>[!tip]- Fallback mechanism :
>>>- can hold a fallback version.
>>>- can hold the new version if the primary boot loader doesn't support OTA
>---
>>[!bug]- Implementation :
>>- 1 :
>>	- تهيئ البوت لودر الثانوي عشان يشتغل مع كل مرة ترستر الجهاز ويشتغل بعد ال - primary boot loader (if it fails)
>>	- حاجة زي if & else
>>- 2 :
>>	- صمم (SSBL) عشان يستقبل التحديثات ويثبتها.
>>- 3 :
>>	- Verification and Validation to the downloaded system
>>- 4 :
>>	- Error Handling:
>>		- لو حصل مشاكل ف يبقي في امكانية اننا نرجع للنظام القديم بدون مشاكل

---
---

>[!success]- Optional !
>- ممكن نخلي الاتصال full duplex بدل simple duplex عشان نقدر نبعت للسيرفر ال log files بالاخطاء واستخدام ال services
>- هيبقي مكلف شوية بس هيساعد بشكل كبير علي تتبع الاخطاء بشكل مباشرز
>---
>- full duplex -> is to make both devices send and receive data simultaneously.
>- simple duplex -> a device send and other receive only.

---
---

>[!todo]- Hardware Required :
>>[!caution]- Client Device:
>>- The client device uses an **ADuCM4050 EZ-KIT** connected to an **ADF7242** transceiver via the transceiver daughterboard horseshoe connector.
>>- The client device is responsible for performing the OTA update logic, receiving update packets, and updating the firmware.
>---
>>[!caution]- Server Device :
>>- The server setup involves another ADuCM4050 EZ-KIT with an ADF7242 transceiver connected in the same manner as the client.
>>- A Python application running on a Windows PC communicates with the server device via the serial port.
>>- The server device relays packets received from the ADF7242 to the Python application but does not perform any OTA update logic itself.
>---
>- chat gpt says its cost will be about 12000 pound when the dollar was = 30 EGP.



## Resources :

- [Analog.com: Over-the-Air (OTA) Updates in Embedded Microcontroller Applications](https://www.analog.com/en/resources/analog-dialogue/articles/over-the-air-ota-updates-in-embedded-microcontroller-applications.html#:~:text=These%20challenges%2C%20coupled%20with%20the,embedded%20system%20with%20new%20software.)


