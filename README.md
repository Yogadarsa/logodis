# logodis
source code for a listing (logo designer want to ask the client)

bus_name='yd logo maker \nphone number:6382443\n\nquestions\n1.what is your business:',input("enter your business kind:")

tar_aud="\n2.targeted audience are:",input("enter the targeted audience:")
#picture need to represent
val_pic="\n3.value to convey in logo and any picture need to involed in logo",input("enter value to convey in logo and any picture need to involed in logo :")
sty='\n4.logo is appiled any sugestion in style\n(example poster,website,social media) \n',input("enter where the logo is appiled (example poster,website,social media) any sugestion in style :")
col_f="\n5.any specific colour,font",input("enter any specific colour ,font:")
rest="\n6.any restrictions in logo \n(like font,colour)\n",input("enter any restrictions in logo \n(like font,colour):")
ide_proj="\n7.do you have idea on this project",input("any ideas on this project:")
bus_name=bus_name+tar_aud+val_pic+sty+col_f+rest+ide_proj

import functools
import operator


def convert_tuple(a):
    res_str = functools.reduce(operator.add, (a))
    return res_str

astrg = convert_tuple(bus_name)
print(astrg)

text_file = open("data.txt", "a")
n = text_file.write(astrg)
text_file.close()
