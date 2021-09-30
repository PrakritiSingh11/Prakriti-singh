# Prakriti-singh
porosity = [] # blank list
Rwa      = [] # blank list

# true zone resistivity, Rt = 20 (Ω-m) as read from log
Rt       = 20 

# In this case, for limestone tortuosity factor, a = 1.0 and cementation exponent, m = 2.0
m        = 2.0
a        = 1.0

while True:
  phi = input("Enter porosity values (%); Enter 'done' if entries completed ")
  
  if phi == "done":
    break
  
  try:
    phi = float(phi)
    porosity.append(phi)
    
    Rwa.append(phi)

  except:
    print('Invalid input')
  
  continue

Rwa = [x**m*Rt/a for x in Rwa]

print('The Apparent Formation Water Resistivity (Rwa) values are ', Rwa)

print('The Formation Water Resistivity (Rw) = ', min(Rwa))
Enter porosity values (%); Enter 'done' if entries completed 15
Enter porosity values (%); Enter 'done' if entries completed 16
Enter porosity values (%); Enter 'done' if entries completed 17
Enter porosity values (%); Enter 'done' if entries completed 18
Enter porosity values (%); Enter 'done' if entries completed 19
Enter porosity values (%); Enter 'done' if entries completed 11
Enter porosity values (%); Enter 'done' if entries completed 10
Enter porosity values (%); Enter 'done' if entries completed done
The Apparent Formation Water Resistivity (Rwa) values are  [4500.0, 5120.0, 5780.0, 6480.0, 7220.0, 2420.0, 2000.0]
The Formation Water Resistivity (Rw) =  2000.0
