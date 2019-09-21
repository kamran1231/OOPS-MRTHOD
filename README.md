# OOPS-MRTHOD


class Mobile:

    #instnce method
    def __init__(self,brand,model,price):
        self.brand = brand
        self.model = model
        # if price > 0:
        #     self.price = price
        # else:
        #     self.price = 0
        self.price = max(price,0)

    @property
    def display_all(self):
        return f'i have {self.brand} phone, model {self.model} and price is {self.price}'

    @property
    def price(self):
        return self.price

    @price.setter
    def price(self,new_price):
        self.price  = max(new_price,0)

    @classmethod
    def without_string(cls,string):
        brand,model,price = string.split(',')
        return cls(brand,model,price)


mob1 = Mobile('nokia',1100,-2000)
mob1.price = 50
# mob2 = Mobile.without_string('samsung,ccdf,30000')
# print(mob1.price)
# print(mob1.display_all())
# print(mob2.display_all())
print(mob1.price)
# print(mob1.display_all)
