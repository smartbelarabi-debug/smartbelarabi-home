# Dynamic Battery Monitoring Package with Travel Mode

## 🇬🇧 English

### Description

Dynamic Battery Monitoring Package with Travel Mode is a Home Assistant package that automatically discovers battery percentage sensors and provides monitoring across three levels:

- Warning level  
- Critical level  
- Travel readiness  

It is fully dynamic and requires no manual configuration of battery entities.

---

### Features

- Fully dynamic battery detection  
- No manual entity listing required  
- Uses Home Assistant `device_class: battery`  
- Separate thresholds for:
  - Warning  
  - Critical  
  - Travel  
- Provides:
  - Count sensors  
  - List sensors  
  - Binary sensors  
- Portable across different Home Assistant setups  

---

### Repository Structure

/packages/dynamic-battery-monitoring-travel-mode.yaml  
/cards/  
  ├── battery-overview.yaml  
  ├── travel-readiness.yaml  
  └── travel-list.yaml  
/README.md  

---

### What the Package Creates

#### Helpers

- input_number.battery_warning_threshold  
- input_number.battery_critical_threshold  
- input_number.battery_travel_threshold  

#### Sensors

- sensor.battery_warning_count  
- sensor.battery_critical_count  
- sensor.battery_travel_count  
- sensor.battery_warning_list  
- sensor.battery_critical_list  
- sensor.battery_travel_list  

#### Binary Sensors

- binary_sensor.battery_warning_active  
- binary_sensor.battery_critical_active  
- binary_sensor.battery_travel_active  

---

### Requirements

- Home Assistant packages enabled  
- Battery sensors must use `device_class: battery`  
- Battery values must be numeric  

---

### Installation

1. Enable packages in configuration.yaml:

homeassistant:
  packages: !include_dir_named packages

2. Copy the package file to:

/config/packages/dynamic-battery-monitoring-travel-mode.yaml

3. Restart Home Assistant  

4. Verify in Developer Tools → States:
- battery_warning_threshold  
- battery_critical_threshold  
- battery_travel_threshold  
- battery_warning_count  
- battery_critical_count  
- battery_travel_count  

---

### Configuration

You can adjust thresholds directly from Home Assistant UI:

- Warning Threshold → general monitoring  
- Critical Threshold → urgent alerts  
- Travel Threshold → pre-travel preparation  

---

### How Travel Mode Works

When a battery level is **below or equal to the travel threshold**:

- It appears in `sensor.battery_travel_list`  
- It is counted in `sensor.battery_travel_count`  
- `binary_sensor.battery_travel_active` turns ON  

---

### Recommended Travel Threshold Guide

- 1–2 days → 30–35%  
- 1 week → 40%  
- 2 weeks → 50%  
- 1 month → 60%  

---

### Example Usage

#### Daily Monitoring

Check:
- sensor.battery_warning_list  
- sensor.battery_critical_list  

#### Before Travel

1. Set travel threshold  
2. Review `sensor.battery_travel_list`  
3. Replace batteries if needed  

---

### Dashboard Cards

Example cards are provided in the `/cards/` folder.

To use them:

1. Open Home Assistant dashboard  
2. Click **Edit Dashboard**  
3. Add **Manual Card**  
4. Paste YAML from the card files  

---

### Troubleshooting

- Ensure `device_class: battery` exists  
- Ensure sensor values are numeric  
- Restart Home Assistant after installation  
- Some integrations may not expose battery correctly  

---

### Why This Package Uses device_class

Using `device_class: battery` ensures:

- Reliable detection  
- No dependency on naming  
- Compatibility across integrations  

---

## 🇸🇦 العربية

### الوصف

هذه الحزمة توفر نظام مراقبة ديناميكي للبطاريات داخل Home Assistant بدون الحاجة لإدخال الأجهزة يدويًا، وتدعم ثلاث مستويات:

- مستوى التنبيه  
- المستوى الحرج  
- وضع الاستعداد للسفر  

---

### المميزات

- اكتشاف تلقائي للبطاريات  
- لا حاجة لإضافة الأجهزة يدويًا  
- يعتمد على `device_class: battery`  
- يدعم ثلاث مستويات (تنبيه - حرج - سفر)  
- يوفر:
  - عدد الأجهزة  
  - قائمة الأجهزة  
  - حساسات منطقية  

---

### المتطلبات

- تفعيل خاصية packages في Home Assistant  
- الأجهزة يجب أن تستخدم `device_class: battery`  
- القيم يجب أن تكون رقمية  

---

### طريقة التثبيت

1. تفعيل packages في configuration.yaml  

2. وضع الملف في المسار:

/config/packages/dynamic-battery-monitoring-travel-mode.yaml  

3. إعادة تشغيل Home Assistant  

4. التحقق من ظهور الحساسات  

---

### وضع السفر

عند انخفاض البطارية عن القيمة المحددة:

- تظهر في قائمة الأجهزة  
- يتم احتسابها  
- يتم تفعيل حالة التنبيه  

---

### التوصيات للسفر

- يوم إلى يومين: 30–35%  
- أسبوع: 40%  
- أسبوعين: 50%  
- شهر: 60%  

---

### ملاحظات

- بعض التكاملات قد لا تعرض البطارية بشكل صحيح  
- تأكد من أن القيم رقمية  
- أعد تشغيل النظام بعد التثبيت  
