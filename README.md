# Madteas
Number 2 this goodpleaseee


// Creating a fake object is very easy!
// No mocks, or stubs; everything's a fake.
var shop = A.Fake<ICandyShop>();

// Easily set up a call to return a value.
var lollipop = new Lollipop();
A.CallTo(() => shop.GetTopSellingCandy()).Returns(lollipop);

// Exercise your system under test by using the fake as you
// would an instance of the faked type.
var customer = new SweetTooth();
customer.BuyTastiestCandy(shop);

// Asserting uses the same syntax as configuring calls.
A.CallTo(() => shop.BuyCandy(lollipop)).MustHaveHappened();
