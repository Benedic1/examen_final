print("Bienvenido en nuestro Inversion")
print("utiliza doble paraa identificar los departamento\n EJEMPLO: A=AA ; B=BB")
verall=['1--Inversion','2---ver disponibilidad departamento','3---ir en ganancia del negocio',
        '4----ver lista arrendador','5---ver lista comprador','6---ver desarollador','7---salir de sistema']
veralls=['1---Arrendar departamento','2---Comprar Departamento']
ref_for_sales=(1,'\t\tDD1\t\tA1D','\t\tDD2\t\tB1D','\t\tDD3\t\tC1D','\t\tDD4\t\tD1D',
               2,'\t\tDD6\t\tA2D','\t\tDD7\t\tB2D','\t\tDD8\t\tC2D','\t\tDD9\t\tD2D',
               3,'\t\tDD11\t\tA3D','\t\tDD12\t\tB3D','\t\tDD13\t\tC3D','\t\tDD14\t\tD3D',
               4,'\t\tDD16\t\tA4D','\t\tDD17\t\tB4D','\t\tDD18\t\tC4D','\t\tDD19\t\tD4D',
               5,'\t\tDD21\t\tA5D','\t\tDD22\t\tB5D','\t\tDD23\t\tC5D','\t\tDD24\t\tD5D',
               6,'\t\tDD26\t\tA6D','\t\tDD27\t\tB6D','\t\tDD28\t\tC6D','\t\tDD29\t\tD6D',
               7,'\t\tDD31\t\tA7D','\t\tDD32\t\tB7D','\t\tDD33\t\tC8D','\t\tDD34\t\tD7D',
               8,'\t\tDD36\t\tA8D','\t\tDD37\t\tB8D','\t\tDD38\t\tC8D','\t\tDD39\t\tD8D',
               9,'\t\tDD40\t\tA9D','\t\tDD41\t\tB9D','\t\tDD42\t\tC9D','\t\tDD43\t\tD9D',
               10,'\t\tDD45\t\tA10D','\t\tDD46\t\tB10D','\t\tDD47\t\tC10D','\t\tDD48\t\tD10D')








total_arriendo=[]
total_venta=[]

cliente_arrendatario=[1]
cliente_arrendatario.sort()
cliente_comprador=[1]
id_cliente_arrendatario=[]
id_cliente_arrendatario.sort()
id_cliente_comprador=[]
id_cliente_comprador.sort()
cliente_comprador.sort()
x=(ref_for_sales[1:])
id_cliente=[]


m=[3,2,7,6,5,4,3,2,0]
mm=[3,2,7,6,5,4,3]
s=0
sa=0                
d=0
da=0
dda=0
xdd=0

suma=0


                
def confirmar():
    print("1--si")
    print("2--no")

class for_rent():

         def __init__(self,*args):
        
             self.price_rent=args[0]
             self.price_sales=args[1]
             self.piso=args[2]
             self.tipo=args[3]

       
f=for_rent(25,3800,'PISO','VENTA')
g=for_rent(18,3200,'PISO','VENTA')
h=for_rent(16,3100,'PISO','VENTA')
i=for_rent(23,3000,'PISO','VENTA')
j=for_rent(28,3400,'PISO','VENTA')





def itemval(fortrue_real):    
    
    itenn=0
    itt=len(fortrue_real)
    if itt == 9:
       for master_i in range(len(m)):
           yield itenn
           itenn +=(int(m[master_i])*int(fortrue_real[master_i]))  
         
    if itt == 8 :
        for other_i in range(len(mm)):
            yield itenn
            itenn +=(int(mm[other_i])*int(fortrue_real[other_i]))
            

def itemvalues(fortrue_real) :
    
    rt=False
    for a in fortrue_real:
        a=len(fortrue_real)
        if a > 7 or a == 9 :
            rt=True
    if not rt:
        print("invalido")
    
            
for isd in range(len(ref_for_sales)):
    
    if isd in ref_for_sales :
        
       deptav1=ref_for_sales.index(isd)
       
       deptav_list1=ref_for_sales[deptav1]
       
       for idr in range(1,5):
           
           detta=ref_for_sales[(deptav1)+(idr)]
           
           xdd +=detta.count('DD')
           
           

    
           
print("TOTAL DEPARTAMENTO:",xdd)

while True:
   for itt in verall :
       print(itt)
   ittar=int(input("seleccionar una opcion\n"))
   if ittar == 1:
       for itr in veralls:
           print(itr)
       ita=int(input("seleccionar opcion\n"))
       
       if ita == 1:
           
          itgs=int(input("ingrese numero de piso"))
          if itgs in ref_for_sales :
             send_request=ref_for_sales.index(itgs)
             send_request1=ref_for_sales[send_request]
             print(f"estas en PISO:--> {itgs}")
             print("slect,\t\tESTADO\t\tTIPO DEPART\n")
             
             for itd in range(1,5) :
                 send_response=ref_for_sales[(send_request)+itd]
                 print(itd,send_response)
             itdr=input("ingrese el tipo departamento porfavor dobla la letra.\n ejemplo F1 = FF1\n")
             revis1=itdr[-1]
             if itdr in cliente_arrendatario :
                print("Depart ya arrendado")
             elif itdr in cliente_comprador:
                 print("Depart ya vendido")
             else:
                while True:
                 
                   fortrue_real =input("ingrese su rut")
                   itemvalues(fortrue_real)
                   itemval(fortrue_real)
                   f=fortrue_real[-1]
                   for vs in itemval(fortrue_real):
                       t=vs%11
                       ts=11-(vs%11)
                   if (int(t))!= (int(f)) and (int(ts))!=(int(f)) and (t)!= (int(f)):
                       print("rut invalido")
                   else :
                       
                       name=input("ingrese el nombre del arrendador\n")
                       piso_ed1=input("ingrese numero de piso\n")
                       napi=int(piso_ed1)*int(revis1)
                       suma +=1
                       id_cliente.append(fortrue_real)
                       cliente_arrendatario.append(itdr[:-1])
                       cliente_arrendatario.append(int(fortrue_real[:-1]))
                       cliente_arrendatario.append([f"TIPO DEPARTAMENTO:\t\t{itdr}",f"RUT ARRENDADOR:\t\t{fortrue_real}",f"{name}"])
                       
                       for cambia in range(len(ref_for_sales)):
                          if cambia in ref_for_sales :
                             fcasa=ref_for_sales.index(cambia)
                             for cambias in range(1,6):
                                 fcass=ref_for_sales[(fcasas)+cambias]
                                 faco=fcass.replace('DD','V',num)
                       break
              

                 
       if ita == 2 :

           itgsa=int(input("ingrese numero de piso"))
           if itgsa in ref_for_sales :
             send_request=ref_for_sales.index(itgsa)
             send_request1=ref_for_sales[send_request]
             print(f"estas en PISO:--> {itgsa}")
             print("slect,\t\tESTADO\t\tTIPO DEPART\n")
             for itd in range(1,5) :
                 send_response=ref_for_sales[(send_request)+itd]
                 print(itd,send_response)
               
           itdrsa=input("ingrese el tipo departamento, porfavor dobla la letra.\n ejemplo F1 = FF1\n")
           revis=itdrsa[-1]
           
           revischange=revis
           if itdrsa in cliente_arrendatario :
               print("Depart ya arrendado")
           elif itdrsa in cliente_comprador:
                 print("Depart ya vendido")
           else:
               while True:
                 fortrue_real =input("ingrese su rut\n")
                 itemvalues(fortrue_real)
                 itemval(fortrue_real)
                 f=fortrue_real[-1]
                 
                 for vs in itemval(fortrue_real):
                     t=vs%11
                     ts=11-(vs%11)
                 if (int(t))!= (int(f)) and (int(ts))!=(int(f)):
                     print("rut invalido")
                 else :
                     
                   name1=input("ingrese el nombre del arrendador\n")
                   
                   piso_ed=int(input("ingrese el numero piso\n"))
                   num=int(revis)*int(piso_ed)
                   id_cliente.append(fortrue_real)
                   cliente_comprador.append(itdrsa[:-1])
                   cliente_comprador.append(int(fortrue_real[:-1]))
                   cliente_comprador.append([f"TIPO DEPARTAMENTO:{itdrsa}",f"RUT ARRENDADOR:{fortrue_real}",f"{name1}"])
                   
                   break
                  

                                                 

               

   if ittar == 2 :
       
       sprie =int(cliente_arrendatario.count('FF'))
       aprime =int(cliente_arrendatario.count('GG'))
       dprime =int(cliente_arrendatario.count('HH'))
           
       cprime =int(cliente_arrendatario.count('II'))
       eprime =int(cliente_arrendatario.count('JJ'))
       bprime =cliente_comprador.count('FF')
       fprime =int(cliente_comprador.count('GG'))
       gprime =int(cliente_comprador.count('HH'))
           
       hprime =int(cliente_comprador.count('II'))
       iprime =int(cliente_comprador.count('JJ'))
       
       consprime=int(sprie)+int(aprime)+int(dprime)+int(cprime)+int(eprime)+int(bprime)+int(fprime)+int(gprime)+int(hprime)+int(iprime)
       print("TOTAL DEPARTAMENTO OCUPADO:",consprime)
       print("TOTAL DEPARTMENTO NO OCUPADO:",int(consprime)- 50)
       
       
       
            

       
                   
   if ittar == 3 :
       
       s =cliente_arrendatario.count('FF')
       sa =int(cliente_arrendatario.count('GG'))
       d =int(cliente_arrendatario.count('HH'))
           
       da =int(cliente_arrendatario.count('II'))
       dda =int(cliente_arrendatario.count('JJ'))
       s1 =cliente_comprador.count('FF')
       sa1 =int(cliente_comprador.count('GG'))
       d1 =int(cliente_comprador.count('HH'))
           
       da1 =int(cliente_comprador.count('II'))
       dda1 =int(cliente_comprador.count('JJ'))
       
       
       class for_rent():

         def __init__(self,*args):
        
             self.price_rent=args[0]
             self.price_sales=args[1]
             self.piso=args[2]
             self.tipo=args[3]

       
       f=for_rent(25,3800,'PISO','VENTA')
       g=for_rent(18,3200,'PISO','VENTA')
       h=for_rent(16,3100,'PISO','VENTA')
       i=for_rent(23,3000,'PISO','VENTA')
       j=for_rent(28,3400,'PISO','VENTA')

       #==============================================================================================================
       # CALCULAR PRECIO DE DEPARTAMENTO ARRENDADO
       
       #==============================================================================================================
       
       print("TIPO DEPARTMENTO\tPRECIO\t\tCANTIDAD\t\tTOTAL")
       print(f"DEPARTAMENTO F VENDIDO:\t{f.price_sales}UF\t\t\t",s,"\t\t",int(s)*int(f.price_sales),"UF")
       print(f"DEPARTAMENTO G VENDIDO:\t{g.price_sales}UF\t\t\t",sa,"\t\t",int(sa)*int(g.price_sales),"UF")
       print(f"DEPARTAMENTO H VENDIDO:\t{h.price_sales}UF\t\t\t",d,"\t\t",int(d)*int(h.price_sales),"UF")
       print(f"DEPARTAMENTO I VENDIDO:\t{i.price_sales}UF\t\t\t",da,"\t\t",int(da)*int(i.price_sales),"UF")
       print(f"DEPARTAMENTO J VENDIDO:\t{j.price_sales}UF\t\t\t",dda,"\t\t",int(dda)*int(j.price_sales),"UF")
       print("__________________________________________________________________________\n")

       seer=int(s)*int(f.price_sales)+int(sa)*int(g.price_sales)+int(d)*int(h.price_sales)+int(da)*int(i.price_sales)+int(dda)*int(j.price_sales)

       seera=int(s)+int(sa)+int(d)+int(da)+int(dda)
       print("TOTAL : \t\t\t\t\t",seera,"\t\t",seer,"UF")
       
       #===============================================================================================================
       #CALCULAR PRECIO DE DEPARTAMENRO  VENDIDO
       
       #===============================================================================================================
       print()
       print("DATOS DE DEPARTAMENTO ARRENDADO\n")
       print("TIPO DEPARTMENTO\tPRECIO\t\tCANTIDAD\t\tTOTAL\n")
       print(f"DEPARTAMENTO F VENDIDO:\t{f.price_rent}UF\t\t\t",s1,"\t\t",int(s1)*int(f.price_rent),"UF")
       print(f"DEPARTAMENTO G VENDIDO:\t{g.price_rent}UF\t\t\t",sa1,"\t\t",int(sa1)*int(g.price_rent),"UF")
       print(f"DEPARTAMENTO H VENDIDO:\t{h.price_rent}UF\t\t\t",d1,"\t\t",int(d1)*int(h.price_rent),"UF")
       print(f"DEPARTAMENTO I VENDIDO:\t{i.price_rent}UF\t\t\t",da1,"\t\t",int(da1)*int(i.price_rent),"UF")
       print(f"DEPARTAMENTO J VENDIDO:\t{j.price_rent}UF\t\t\t",dda1,"\t\t",int(dda1)*int(j.price_rent),"UF")
       print("________________________________________________________________________")

       seeras=int(s1)*int(f.price_rent)+int(sa1)*int(g.price_rent)+int(d1)*int(h.price_rent)+int(da1)*int(i.price_rent)+int(dda1)*int(j.price_rent)
       seeeras=int(s1)+int(sa1)+int(d1)+int(da1)+int(dda1)

       print("TOTAL : \t\t\t\t\t",seeeras,"\t\t",seeras,"UF")
       





   if ittar == 4:
       
       id_cliente_arrendatario.sort()  
       for i in id_cliente_arrendatario:
           
           for iyt in range(1):
              print(i)
              
       print("1--filtrar por rut")
       print("2--terminar proceso")
       
       filtar_rut=int(input("seleccion una opcion\n"))
       if filtar_rut == 1:
          try:
              
            rent_docx_for=int(input("Ingrese el rut sin varificador\n"))
            for_rent_look=rent_docx_for
       
            if for_rent_look in cliente_arrendatario :
                rent_looks=cliente_arrendatario.index(for_rent_look)
                rent_looksa=cliente_arrendatario[(rent_looks)+1]
                
                for xrent_look in rent_looksa:
                    
                    print( xrent_look)
                       
          except:

            print("el rut buscado no existe")

       if filtar_rut == 2 :
           print("has terminado el proceso")
           break

   if ittar == 5 :

       for id_i in id_cliente_comprador :
           for id_ir in range(1):
               print(id_i)
       print("seleciona una opcion")
       print("1--filtrar por rut")
       print("2--terminar proceso")
       
       filtrar_comp=int(input("selecciona una opcion\n"))
       
       if filtrar_comp == 1:
           
          try:
             
            rent_docxc=int(input("ingrese rut sin digit verificador\n"))
            
            if rent_docxc in cliente_comprador :
                
               rent_fil=cliente_comprador.index(rent_docxc)
               rent_fil_next=cliente_comprador[(rent_fil)+1]
               for xrent_fil in rent_fil_next:
                   
                   print(rent_fil)
                         
          except:
             print("el id buscado no existe")
               
           
   if ittar == 6 :
       
       from datetime import date
       

       fecha_dia= date.today()
       print(f"NOMBRE DESARROLLADOR:\t\t BENEDIC JEAN\n INSTITUCION:\t\t\tDUOC UC\nFECHA:\t\t\t{fecha_dia}")

   if ittar == 7 :
      print("Gracias por visitarnos y hacer negocio con nosotros")
      print("Te esperamos por una proxima visita")
      break

