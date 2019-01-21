# earlycodes
# A representation of simple operations of a Bank Account

class BankAccount(object):
  balance = 0
  def __init__(self, name):
    self.name = name
    
  def __repr__(self):
    return "The account belongs to %s and has $%.2f" % (self.name, self.balance)
  
  def show_balance(self):
    print "Account Balance: $%.2f" % (self.balance)
    
  def deposit(self, amount):
    self.amount = amount
    if amount <= 0:
      print "Invalid Amount!"
      return
    else:
      print "$%.2f has been deposited" % (self.amount)
      self.balance += amount
      self.show_balance()
      
  def withdraw(self, amount):
    self.amount = amount
    if amount > self.balance:
      print "Insufficent Funds"
      return
    else:
      print "Withdrawing: $%.2f" % (self.amount)
      self.balance -= amount
      self.show_balance()
      
my_account = BankAccount("Daniel Ukene")
print my_account
my_account.show_balance
my_account.deposit(2000)
my_account.withdraw(1000)
print my_account
