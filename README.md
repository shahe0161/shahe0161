# function to validate age greater than years a member
def fixer (Age):
while True:
try:
print("Please enter how long you have been a member (in years)")
yearsMember = int(input())
except ValueError:
print("not a whole year")
else:
if yearsMember > Age:
print ("not a whole number")
else:
print("")
return yearsMember
# membership function plus activity
def MemberShip (membershipCount,membershipIncome):
correct = False
# get age
while correct == False:
try:
print("Please enter your Age")
Age = int(input())
except ValueError:
print ("not a whole number")
else:
correct = True
print()
#get name
print("Please enter your Name ")
Name = input()
print()
# junior membership
if Age <= 18:
MemberType = "Junior"
print("You have a", MemberType, "MemberShip")
Year = False
yearsMember = fixer (Age)
if yearsMember >= 2:

cost = 40
print("It will cost you £",cost,"per year")
else:
cost = 60
print("It will cost you £",cost,"per year")
print()
print("Would you like to proceed with the membership (Y/N")
Answer = input()
if Answer.upper() == "Y":
print("It will cost you £",cost,"per year")
membershipCount += 1
membershipIncome += cost
print("Would you like to do an activity")
Answer = input()
if Answer.upper() == "Y":
active = False
while active == False:
Swimming = 2.80
Gym = 0.00
softPlay = 2.00
print("Pick what activity would you like to do down below")
my_list = ['Swimming cost £2.80','Gym cost £0.00','Soft Play cost £2.00']
print("s = Swimming, g = Gym, p = Soft Play")
print(my_list[0]) # Swimming
print(my_list[1]) # Gym
print(my_list[2]) # Soft Play
Activity = input()
if Activity.upper() == "S":
print("This Activity cost £ {:.2f}".format(Swimming))
print("Would you like to proceed with the payment")
Answer = input()
if Answer.upper() == "Y":
print("It will cost you £ {:.2f}".format(Swimming))
Total = cost + Swimming
print ("Total cost £ {:.2f}".format(Total))
active = True
else:
print("would you like to do another activity ")

Activity = input()
if Activity.upper() == "P":
print("This Activity cost £ {:.2f}".format(softPlay))
print("Would you like to proceed with the payment")
Answer = input()
if Answer.upper() == "Y":
print("It will cost you £ {:.2f}".format(softPlay))
Total = cost + softPlay
print ("Total cost £ {:.2f}".format(Total))
active = True
else:
print("would you like to do another activity ")

elif Activity.upper() == "G":
print("This Activity cost £ {:.2f}".format(Gym))
print("Would you like to proceed with the payment")
Answer = input()
if Answer.upper() == "Y":
print("It will cost you £ {:.2f}".format(Gym))
active = True
else:
print("would you like to do another activity ")
else:
print("bad")
else:
print("Done")
return membershipCount,membershipIncome
else:
print("why")

# Senior membership
elif Age < 50:
MemberType = "Senior"
print("You have a", MemberType, "MemberShip")
Year = False
while Year == False:
try:
yearsMember = fixer (Age)
except ValueError:
print("not a whole year")

else:
Year = True
if yearsMember >= 10:
cost = 90
print("It will cost you £",cost,"per year")
else:
cost = 120
print("It will cost you £",cost,"per year")
print()
print("Would you like to proceed with the membership (Y/N")
Answer = input()
if Answer.upper() == "Y": # proceed
print("It will cost you £",cost,"per year")
membershipCount += 1
membershipIncome += cost
print("Would you like to do an activity")
Answer = input()
# Activity
if Answer.upper() == "Y":
active = False
while active == False:
Swimming = 3.80
Gym = 0.00
print("Pick what activity would you like to do down below")
my_list = ['Swimming cost £2.80','Gym cost £0.00']
print("s = Swimming, g = Gym")
print(my_list[0]) # Swimming
print(my_list[1]) # Gym
Activity = input()
if Activity.upper() == "S": #activity swim
print("This Activity cost £ {:.2f}".format(Swimming))
print("Would you like to proceed with the payment")
Answer = input()
if Answer.upper() == "Y": #proceed
print("It will cost you £ {:.2f}".format(Swimming))
Total = cost + Swimming
print ("Total cost £ {:.2f}".format(Total))
active = True
else: #proceed

print("would you like to do another activity ")

elif Activity.upper() == "G": #activity gym
print("This Activity cost £ {:.2f}".format(Gym))
print("Would you like to proceed with the payment")
Answer = input()
if Answer.upper() == "Y":
print("It will cost you £ {:.2f}".format(Gym))
active = True
else:
print("would you like to do another activity ")
else: # activity non
print("bad")
else:
print("done")
return membershipCount,membershipIncome
else: # proceed
print("why")

# veteran membership
else:
MemberType = "Veteran"
print("You have a", MemberType, "MemberShip")
Year = False
yearsMember = fixer (Age)
if yearsMember >= 10:
cost = 50
print("The cost is £",cost,"per year")
else:
cost = 80
print("The cost is £",cost,"per year")
print()
print("Would you like to proceed with the membership (Y/N")
Answer = input()

if Answer.upper() == "Y":
print("It will cost you £",cost,"per year")
membershipCount += 1
membershipIncome += cost
print("Would you like to do an activity")
Answer = input()
if Answer.upper() == "Y":
active = False
while active == False:
Swimming = 2.80
Gym = 0.00
print("Pick what activity would you like to do down below")
my_list = ['Swimming cost £2.80','Gym cost £0.00']
print("s = Swimming, g = Gym")
print(my_list[0]) # Swimming
print(my_list[1]) # Gym
Activity = input()
if Activity.upper() == "S":
print("This Activity cost £ {:.2f}".format(Swimming))
print("Would you like to proceed with the payment")
Answer = input()
if Answer.upper() == "Y":
print("It will cost you £ {:.2f}".format(Swimming))
Total = cost + Swimming
print ("Total cost £ {:.2f}".format(Total))
active = True
else:
print("would you like to do another activity ")

elif Activity.upper() == "G":
print("This Activity cost £ {:.2f}".format(Gym))
print("Would you like to proceed with the payment")
Answer = input()
if Answer.upper() == "Y":
print("It will cost you £ {:.2f}".format(Gym))
active = True
else:
print("would you like to do another activity ")
else:
print("bad")

else:
print("done")
return membershipCount,membershipIncome
else:
print("why")
# non member activity function
def NoneMemberShip (ActivityCount,ActivityIncome):
correct = False
while correct == False:
try:
print("Please enter your Age")
Age = int(input())
except ValueError:
print ("not a whole number")
else:
correct = True
print()
print("Please enter your Name ")
Name = input()
print()

if Age <= 18:

Gym = 5.00
softPlay = 3.00
print("Pick what activity would you like to do down below")
my_list = ['Swimming cost £2.80','Gym cost £0.00']
print("p = softPlay, g = Gym")
print(my_list[0])
print(my_list[1])
Activity = input()
if Activity.upper() == "P":
print("This Activity cost £ {:.2f}".format(softPlay))
print("Would you like to proceed with the payment")
Answer = input()
if Answer.upper() == "Y":

print("It will cost you £ {:.2f}".format(softPlay))
ActivityCount += 1
ActivityIncome += softPlay

if Activity.upper() == "G":
print("This Activity cost £ {:.2f}".format(Gym))
print("Would you like to proceed with the payment")
Answer = input()
if Answer.upper() == "Y":
print("It will cost you £ {:.2f}".format(Gym))
ActivityCount += 1
ActivityIncome += Gym

if Age < 50:
Gym = 10.00
Swimming = 4.20
print("Pick what activity would you like to do down below")
my_list = ['Swimming cost £4.20','Gym cost £10.00']
print("s = Swimming, g = Gym")
print(my_list[0])
print(my_list[1])
Activity = input()
if Activity.upper() == "S":
print("This Activity cost £ {:.2f}".format(Swimming))
print("Would you like to proceed with the payment")
Answer = input()
if Answer.upper() == "Y":
print("It will cost you £ {:.2f}".format(Swimming))
ActivityCount += 1
ActivityIncome += Swimming

Activity = input()
if Activity.upper() == "G":
print("This Activity cost £ {:.2f}".format(Gym))
print("Would you like to proceed with the payment")

Answer = input()
if Answer.upper() == "Y":
print("It will cost you £ {:.2f}".format(Gym))
ActivityCount += 1
ActivityIncome += Gym

if Age >= 50:
Gym = 7.00
print("Pick what activity would you like to do down below")
my_list = ['Gym cost £10.00']
print("g = Gym")
print(my_list[0])
Activity = input()
if Activity.upper() == "G":
print("This Activity cost £ {:.2f}".format(Gym))
print("Would you like to proceed with the payment")
Answer = input()
if Answer.upper() == "Y":
print("It will cost you £ {:.2f}".format(Gym))
ActivityCount += 1
ActivityIncome += Gym
return ActivityCount,ActivityIncome

# member activity function
def MemberShipActivity (ActivityCount,ActivityIncome):
correct = False
while correct == False:
try:
print("Please enter your Age")
Age = int(input())
except ValueError:
print ("not a whole number")
else:
correct = True
print()

print("Please enter your Name ")
Name = input()
print()

if Age <= 18:
active = False
while active == False:
Gym = 0.00
softPlay = 2.00
print("Pick what activity would you like to do down below")
my_list = ['softPlay cost £2.00','Gym cost £0.00']
print("p = softPlay, g = Gym")
print(my_list[0])
print(my_list[1])
Activity = input()
if Activity.upper() == "P":
print("This Activity cost £ {:.2f}".format(softPlay))
print("Would you like to proceed with the payment")
Answer = input()
if Answer.upper() == "Y":
print("It will cost you £ {:.2f}".format(softPlay))
ActivityCount += 1
ActivityIncome += softPlay
active = True
else:
print("would you like to do another activity ")
Activity = input()
if Activity.upper() == "G":
print("This Activity cost £ {:.2f}".format(Gym))
print("Would you like to proceed with the payment")
Answer = input()
if Answer.upper() == "Y":
print("It will cost you £ {:.2f}".format(Gym))
active = True
else:
print("would you like to do another activity ")

if Age < 50:

print ("Would you like to do an activity")
Answer = input()
if Answer.upper() == "Y":
active = False
while active == False:
Gym = 0.00
Swimming = 3.80
print("Pick what activity would you like to do down below")
my_list = ['Swimming cost £3.80','Gym cost £0.00']
print("s = Swimming, g = Gym")
print(my_list[0])
print(my_list[1])
Activity = input()
if Activity.upper() == "S":
print("This Activity cost £ {:.2f}".format(Swimming))
print("Would you like to proceed with the payment")
Answer = input()
if Answer.upper() == "Y":
print("It will cost you £ {:.2f}".format(Swimming))
ActivityCount += 1
ActivityIncome += Swimming
active = True
else:
print("would you like to do another activity ")
Activity = input()
if Activity.upper() == "G":
print("This Activity cost £ {:.2f}".format(Gym))
print("Would you like to proceed with the payment")
Answer = input()
if Answer.upper() == "Y":
print("It will cost you £ {:.2f}".format(Gym))
active = True
else:
print("would you like to do another activity ")

if Age >= 50:
print ("Would you like to do an activity")
Answer = input()
if Answer.upper() == "Y":
active = False

while active == False:
Gym = 0.00
print("Pick what activity would you like to do down below")
my_list = ['Gym cost £0.00']
print("g = Gym")
print(my_list[0])
Activity = input()
if Activity.upper() == "G":
print("This Activity cost £ {:.2f}".format(Gym))
print("Would you like to proceed with the payment")
Answer = input()
if Answer.upper() == "Y":
print("It will cost you £ {:.2f}".format(Gym))
ActivityCount += 1
ActivityIncome += Gym
active = True
else:
print("would you like to do another activity ")

return ActivityCount,ActivityIncome

#### main program ###
membershipCount = 0
membershipIncome = 0
ActivityCount = 0
ActivityIncome = 0
rep = False
while rep == False:
print("Do you have a membership")
print("Please enter Y/N")
Answer = input()
if Answer.upper() == "N":
print("Would you like to have a membership")
print("Please enter Y/N")
Answer = input()
if Answer.upper() == "Y":
print()
membershipCount,membershipIncome =
MemberShip(membershipCount,membershipIncome)
print("Would you like to make another transaction")

if Answer.upper() == "Y":
rep = False
else:
rep = True
else:
print("Would you like to do an activity")
Answer = input()
if Answer.upper() == "Y":
ActivityCount,ActivityIncome = NoneMemberShip(ActivityCount,ActivityIncome)
else:
rep = True
else:
print()
Answer = input("Would you like to do an activity ")
if Answer.upper() == "Y":
ActivityCount,ActivityIncome = MemberShipActivity(ActivityCount,ActivityIncome)
else:
print()
rep = True
print("Total Members", membershipCount,"Total member cost", membershipIncome,"Amount of
Actities done", ActivityCount,"Total cost for Activities", ActivityIncome)
