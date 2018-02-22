# cautious-xia
import xdrlib,sys
import xlwt
import xlrd
import numpy as np
#

# file = xlwt.Workbook()
# table = file.add_sheet('info',cell_overwrite_ok=True)
# table.write(0,0,'sssbbb')
# file.save('file.xls')
#新建了一个文件‘file。xls’，在cell （0,0）  里面 输入了数据‘sssbbb’

# 测试下别的功能

data = xlrd.open_workbook('file.xls')
table = data.sheets()[0]

file = xlwt.Workbook()
table = file.add_sheet("123")


for i in range(0,4):
    ex_data = table.row_values(i)
    for j in range(len(ex_data)):
        cell = ex_data[j]

table.write(i,j,cell)

    print(ex_data)
