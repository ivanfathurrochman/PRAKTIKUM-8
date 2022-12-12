
# PRAKTIKUM-8

### Nama : Ivan Fathurrochman 
### Nim : 312210271
### Kelas : TI.22.A2

<img width="600" alt="206861210-6824eb25-af58-4bd3-8469-89d7528af4b3" src="https://user-images.githubusercontent.com/115911604/207039787-afaa2d9d-3da4-480d-ae81-f1e3976eb20f.png">

## Flowchart

![image](https://user-images.githubusercontent.com/115911604/207040139-a4aed94d-750d-4332-a255-aee13efc3032.png)

## Program

import os

class data_mhsw:

nama=""

nim=""
 
tugas=""

uts=""

uas=""
    
data = []

def no_data():
    
    print("DAFTAR NILAI MAHASISWA")

    print("----------------------")
 
    print()

    print(" - TIDAK ADA DATA - ")
   
    print()

def tambah():
   
    os.system("cls")
   
    b = data_mhsw()
   
    print("TAMBAH DATA")
  
    print("------------")
  
    b.nama = (input("Nama Mahasiswa\t: "))
  
    b.nim = (int(input("NIM Mahasiswa\t: ")))
  
    b.tugas = (int(input("Nilai Tugas\t: ")))
   
    b.uts = (int(input("Nilai UTS\t: ")))
   
    b.uas = (int(input("Nilai UAS\t: ")))
    
    b.akhir = (b.tugas*30/100) + (b.uts*35/100) + (b.uas*35/100) 
   
    data.append(b)
   
    print()

def lihat():
   
    os.system("cls")
  
    if len(data) <=0:
   
    no_data()     
  
  else:
   
   for a in data:
      
      print("DAFTAR NILAI MAHASISWA")
      
      print("-----------------------")
      
      print("Nama Mahasiswa\t: "+a.nama)
          
      print("NIM Mahasiswa\t: "+str(a.nim))
       
      print("Nilai Tugas\t: "+str(a.tugas))
      
      print("Nilai UTS\t: "+str(a.uts))
       
      print("Nilai UAS\t: "+str(a.uas))
       
      print("Nilai Akhir\t: "+str(a.akhir))
      
      print()

def hapus():
       
       os.system("cls")
       
       if len(data) <=0:
            no_data()
     
       else:
        
        nama = data_mhsw()
          
          print("HAPUS DATA")
       
          print("----------")
         
          nama = (input("Nama Mahasiswa\t: "))
          
          for nama in data:
                data.remove(nama)
       
          print()

def ubah():
  
  os.system("cls")
    if len(data) <=0:
        no_data()
  
  else:
     
     nama = data_mhsw()
     
     print("UBAH DATA")
     
     print("---------")
      
     nama = (input("Nama Mahasiswa\t: "))
     
     for nama in data:
       
       nama.tugas = (int(input("Nilai Tugas\t: ")))
         
       nama.uts = (int(input("Nilai UTS\t: ")))
         
       nama.uas = (int(input("Nilai UAS\t: ")))
         
       akhir = (nama.tugas*30/100) + (nama.uts*35/100) + (nama.uas*35/100)
      
      print()

Loop = True

while Loop:
    
    print("Pilih Menu")
   
    print("----------")
    
    tanya = input("[(L)ihat, (T)ambah, (U)bah, (H)apus, (K)eluar] : ")
  
    print()

    if tanya=="l" or tanya=="L":
        lihat()
    
    elif tanya=="t" or tanya=="T":
        tambah()
    
    elif tanya=="u" or tanya=="U":
        ubah()
    
    elif tanya=="h" or tanya=="H":
        hapus()
    
    elif tanya=="k" or tanya=="K":
        print("Program Selesai")
        Loop = False
        
  ## Penjelasan
  ### Untuk memanggil fungsi dengan nama "os".

import os

### membuat class data_mhsw dengan atributnya, yaitu nama, nim, tugas, uts dan uas.

class data_mhsw:
   
   nama=""
  
   nim=""
  
   tugas=""
  
   uts=""
   
   uas=""
