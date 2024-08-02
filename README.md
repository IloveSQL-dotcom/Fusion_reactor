# Fusion_reactor
Well, i wanted to make a simulation for a fusion reactor controll terminal that could controll a fusion reactor, but in really of course just like a fun project. Still i wanted to know what you all guys think of it. Is tehre anything to make better?

Python file:

import time
while True:
    print("Hello, welcome to the fusion reactor serives and control terminal of Tokamak Energy, how can I help you today?")
    time.sleep(1)
    welcome = input("choose one of the following --> activate fusion reactor; fusion reactor capazity; fusion reactor fuel tank; fusion reactor help center: ")
    Choices = ['fusion reactor help center','activate fusion reactor','fusion reactor capazity','fusion reactor fuel tank']
    while welcome not in Choices:
        welcome = input("choose one of the following: activate fusion reactor; fusion reactor capazity; fusion reactor fuel tank; fusion reactor help center: ").lower()
    if welcome == "activate fusion reactor":
        Choice2 = ['hydrogen','helium']
        fuel = input("what kind of fuel-gas will be used for the reactor? (hydrogen/helium): ")
        while fuel not in Choice2:
            fuel = input("what kind of fuel-gas will be used for the reactor? (hydrogen/helium): ")
        if fuel == "hydrogen":
            print("reactor is fueling with hydrogen, please wait...")
            time.sleep(5)
        else:
            print("reactor is fueling with helium, please wait...")
            time.sleep(5)
        print("Now activating the Tokamak Energy fusion reactor with {}, please wait...".format(fuel))
        time.sleep(10)
        print("Attention! The Tokamak Energy fusion reactor is now running! Please be aware that nothing breaks the flow of the fusion reactor!")
    if welcome == "fusion reactor capazity":
        Choice3 = ['yes','no']
        yes_no = input("Your fusion reactor is now at the maximum capazity. Do you want to change the capazity of the fuison reactor? (yes/no): ")
        while yes_no not in Choice3:
            yes_no = input("Your fusion reactor is now at the maximum capazity. Do you want to change the capazity of the fuison reactor? (yes/no): ").lower()
        if yes_no == "yes":
            num = int(input("On which percentage you want to have the capazity to be on your fusion reactor?: "))
            if num > 0 and num <= 100:
                print("Please wait, we are putting your fusion reactor on " + str(num) +"%" + " capazity...")
                time.sleep(5)
                print("The fusion reactors capazity was succesfully changed!")
            else:
                num = int(input("On which percentage you want to have the capazity to be on your fusion reactor?: "))
        elif yes_no == "no":
            print("The capazity of your fusion reactor was not changed!")
    if welcome == "fusion reactor fuel tank":
        print("The fusion reactor has now 80 percent of his fuel in it.")
    if welcome == "fusion reactor help center":
        print("The energy-producing mechanism in a fusion reactor is the joining together of two light atomic nuclei. When two nuclei fuse, a small amount of mass is converted into a large amount of energy.")
    play_again = input("Can the fusion reactor control terminal help you with something else with (yes/no)?: ")
    if play_again != "yes":
        break
print("Thank you for using the fusion reactor services from Tokamak Energy and the control terminal for the fusion reactor, see you next time!")
import time, random
while True:
    print("Hello, welcome to the fusion reactor serives and control terminal of Tokamak Energy, the fusion reactor is currently working, what can we help with?")
    time.sleep(1)
    Choice4 = ['checking how much energy was made','turning the fusion reactor off','cheking the fusion reactors fuel tank']
    welcome2 = input("Choose one of the options --> checking how much energy was made; turning the fusion reactor off; cheking the fusion reactors fuel tank: ")
    while welcome2 not in Choice4:
        welcome2 = input("Choose one of the options --> checking how much energy was made; turning the fusion reactor off; cheking the fusion reactors fuel tank: ")
    if welcome2 == "checking how much energy was made":
        Choice5 = ['1','2','3','4','5','6','7','8','9','10','15']
        print("checking...")
        time.sleep(5)
        print(random.choice(Choice5) + "M-watt was made so far with the fusion reactor.")
    if welcome2 == "cheking the fusion reactors fuel tank":
        Choice6 = ['5','10','15','20','25','30','35','40','45','50','55','60','65','70','75','80','85','90','95']
        print("checking...")
        time.sleep(5)
        print("The fusion reactors tank is currently with " + random.choice(Choice6) +  "%"+"fuel-gas in it")
    if welcome2 == "turning the fusion reactor off":
        Choice7 = ["yes","no"]
        YES_NO = None
        while YES_NO not in Choice7:
            YES_NO = input("Are you sure you want to turn off the fusion reactor? (yes/no): ")
        if YES_NO == "yes":
            print("Please wait, the fusion reactor is now turing off...")
            time.sleep(10)
            print("the fusion reactor was now turned off. It is now not working anymore.")
        if YES_NO == "no":
            print("The fusion reactor was not turned off. It is currently working.")
    play_again2 = input("Can the fusion reactor control terminal help you with something else with (yes/no)?: ")
    if play_again2 != "yes":
        break
print("Thank you for using the fusion reactor services from Tokamak Energy and the control terminal for the fusion reactor, see you next time!")
