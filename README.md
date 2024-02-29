# diseased-leaves

โปรเจคนี้เกี่ยวกับการใช้เทคโนโลยีการเรียนรู้ของเครื่อง (Machine Learning) และ Deep Learning ในการสร้างและใช้โมเดลการทำนายภาพเพื่อตรวจสอบโรคในต้นไม้ โดยมีขั้นตอนการทำงานที่สำคัญต่อไปนี้:

การเตรียมข้อมูล:
ใช้ TensorFlow และ PyTorch ในการเตรียมข้อมูลสำหรับการฝึกเทรนและทดสอบโมเดล. ใช้ไลบรารี ImageDataGenerator ของ Keras ในการสร้างข้อมูลฝึกเทรนโดยทำการ augmentation ข้อมูล.

การสร้างและฝึกเทรนโมเดล:
ใช้โมเดล MobileNet ที่ถูกฝึกเทรนล่วงหน้า (pre-trained) ด้วยข้อมูล ImageNet. ทำการ Fine-tuning โมเดลนี้ด้วยข้อมูลภาพของต้นไม้ที่เป็นโรค. บันทึกโมเดลที่ถูกฝึกเทรนเป็นไฟล์ TensorFlow Lite (.tflite) เพื่อให้สามารถนำไปใช้งานในแอปพลิเคชันหรืออุปกรณ์ที่มีทรัพยากรจำกัด.

การทำนายภาพ:
ใช้ TensorFlow Lite Interpreter เพื่อทำนายภาพจากโมเดลที่ถูกบันทึก. แสดงภาพที่ถูกทำนายและผลลัพธ์ที่ได้.

การวิเคราะห์ผลลัพธ์:
แสดงค่าความน่าจะเป็น (probability) และชื่อของคลาสที่ทำนายได้. แสดงกราฟ Loss และ Accuracy ของโมเดลขณะฝึกเทรน.

การใช้ PyTorch:
ใช้ PyTorch ในการเตรียมข้อมูลและการฝึกเทรนโมเดล. ใช้ DataLoader, ImageFolder, และ TensorDataset ในการจัดการข้อมูล.

การบันทึก Class Indices:

การบันทึก Class Indices:
สร้างและบันทึกไฟล์ JSON ที่เก็บข้อมูลของ Class Indices ที่ใช้ในการฝึกเทรน. โปรเจคนี้ทำให้ได้ทดลองการใช้ TensorFlow และ PyTorch ในการสร้างและใช้โมเดลการทำนายภาพ และได้ฝึกเทรนโมเดลด้วยข้อมูลที่เกี่ยวข้องกับการตรวจสอบโรคในต้นไม้และการนำไปใช้งาน
