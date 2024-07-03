

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
>>>---
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
>- هيبقي مكلف شوية بس هيساعد بشكل كبير علي تتبع الاخطاء بشكل مباشر.
>---
>- full duplex -> is to make both devices send and receive data simultaneously.
>- simple duplex -> a device send and other receive only.

---
---

>[!todo]- Suggested Components :
>- `Lo-Fi` :
>- <a href="#"><img src="https://i.kickstarter.com/assets/041/888/282/b89c34d8eea4a056e80ea89d40ef6a2d_original.gif?fit=scale-down&origin=ugc&q=92&width=680&sig=MAp0aS%2FbB1%2FjdnYOPiiDlN3sMMjcu6SnSaSk9%2BdhTFo%3D" alt="Lo-Fi" width="500" height="400"></a>
>---
>>[!caution]- Benefits :
>>- Long range:
>>	- LoRa can communicate over distances of up to 5 kilometers in open areas.
>>---
>>- Low power: 
>>	- LoRa is very power-efficient, which makes it ideal for battery-powered devices.
>>----
>>- Secure: 
>>	- LoRa uses encryption to protect data from unauthorized access.
>>---
>>- Scalable: 
>>	- LoRa networks can be easily scaled to accommodate a large number of devices.
>---
>>[!caution]- Cost :
>>- the three component will cost  70 dollar ~= 3500 pound..
>>- ![[Pasted image 20240703131403.png]]
>---
>>[!bug] Resources :
>>- [Lo-Fi](https://www.kickstarter.com/projects/picobarcodescanner/lo-fi-long-range-wireless-communication-device-with-esp32)

---
---
### A Full Project On OTA :
- [Graduation_Project_2021](https://github.com/mohamed-hafez-mohamed/Graduation_Project_2021)
	- mansoura university 2021
	- an OTA full project

---
---

### Resources :

- [Analog.com: Over-the-Air (OTA) Updates in Embedded Microcontroller Applications](https://www.analog.com/en/resources/analog-dialogue/articles/over-the-air-ota-updates-in-embedded-microcontroller-applications.html#:~:text=These%20challenges%2C%20coupled%20with%20the,embedded%20system%20with%20new%20software.)


