# project6
#ขั้นที่ 3
import random

def generation_customer_name():
  """สุ่มชื่อลูกค้าจำลอง โดยรวมชื่อ+นามสกุลแบบสุ่ม"""
  first_names =["เจสซี่","ลีโอ","มายา","อเล็กซ์","คลาร่า","ลูคัส","นิโคล"]
  last_names =["รักเรียน","ใจดี","สายทอง","รุ่งเรือง","มั่นคง","วงศ์สว่าง","เจริญพร"]
  return random.choice(first_names) + " " + random.choice(last_names)

def random_price(min_price=40.0, max_price=50.0):
  """สุ่มราคากาแฟ/เครื่องดื่ม ระหว่าง min_price ถึง max_price บาท (ปัดทศนิยม 2 ตำแหน่ง)"""
  return round(random.uniform(min_price, max_price),2)

def random_sweetness_level():
  """สุ่มระดับความหวานของเครื่องดื่ม"""
  levels = ["0%","25%","50%","75%","100%"]
  return random.choice(levels)

print(generation_customer_name())
