# w05-using-function-6015261005
=========================================================================
1.cal_days_in_month
<?php
$number = cal_days_in_month(CAL_GREGORIAN, 8, 2003); // 31
echo "There were {$number} days in August 2003";
?>
==========================================================================
ฟังก์ชันนี้จะส่งคืนจำนวนวันในเดือนของปีสำหรับปฏิทินที่ระบุ
ปฏิทิน
ปฏิทินที่ใช้สำหรับการคำนวณ
เดือน
เดือนในปฏิทินที่เลือก
ปี
ปีในปฏิทินที่เลือก
==========================================================================
2.cal_from_jd
<?php
$today = unixtojd(mktime(0, 0, 0, 8, 16, 2003));
print_r(cal_from_jd($today, CAL_GREGORIAN));
?>
==========================================================================
cal_from_jd () แปลงวัน Julian ที่กำหนดใน jd เป็นวันที่ของปฏิทินที่ระบุ 
ค่าปฏิทินที่รองรับคือ CAL_GREGORIAN, CAL_JULIAN, CAL_JEWISH และ CAL_FRENCH

JD
วันจูเลียนเป็นจำนวนเต็ม
ปฏิทิน
ปฏิทินที่จะแปลงเป็น
Return Values 
ส่งคืนอาร์เรย์ที่มีข้อมูลปฏิทินเช่นเดือน, วัน, ปี, วันของสัปดาห์ (dow), 
ตัวย่อและชื่อเต็มของวันทำงานและเดือนและวันที่ในรูปแบบสตริง "เดือน / วัน / ปี" วันของสัปดาห์มีตั้งแต่ 0 (วันอาทิตย์) ถึง 6 (วันเสาร์)
==========================================================================
3.cal_info
<?php
$info = cal_info(0);
print_r($info);
?>
==========================================================================
cal_info () ส่งคืนข้อมูลในปฏิทินที่ระบุ
ข้อมูลปฏิทินถูกส่งคืนเป็นอาร์เรย์ที่มีองค์ประกอบ calname, calsymbol, เดือน, abbrevmonth และ maxdaysinmonth
ชื่อของปฏิทินที่แตกต่างกันซึ่งสามารถใช้เป็นปฏิทินมีดังนี้
0 หรือ CAL_GREGORIAN 
1 หรือ CAL_JULIAN 
2 หรือ CAL_JEWISH 
3 หรือ CAL_FRENCH 
หากไม่มีการระบุข้อมูลปฏิทินในปฏิทินที่สนับสนุนทั้งหมดจะถูกส่งคืนเป็นอาร์เรย์
==========================================================================
4.cal_to_jd
cal_to_jd ( int $calendar , int $month , int $day , int $year ) : int
==========================================================================
cal_to_jd - แปลงจากปฏิทินที่รองรับเป็นจำนวนวัน
cal_to_jd () คำนวณการนับวัน สำหรับวันที่ในปฏิทินที่ระบุ
ปฏิทิน
ปฏิทินที่จะแปลงหนึ่งใน CAL_GREGORIAN, CAL_JULIAN, CAL_JEWISH หรือ CAL_FRENCH

เดือน
เดือนเป็นตัวเลขช่วงที่ถูกต้องขึ้นอยู่กับปฏิทิน

วัน
วันเป็นตัวเลขช่วงที่ถูกต้องขึ้นอยู่กับปฏิทิน

ปี
ปีเป็นตัวเลขช่วงที่ถูกต้องขึ้นอยู่กับปฏิทิน
==========================================================================
5.DateTime::add
<?php
$date = new DateTime('2000-01-01');
$date->add(new DateInterval('P10D'));
echo $date->format('Y-m-d') . "\n";
?>
==========================================================================
DateTime :: เพิ่ม - date_add - เพิ่มจำนวนวันเดือนปีชั่วโมงนาทีและวินาทีให้กับวัตถุ
