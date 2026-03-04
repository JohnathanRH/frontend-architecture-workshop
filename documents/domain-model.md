# Domain Model

## Entities

- `Customer`
-  `Session`
- `Restaurant`
- `RestaurantCategory`
- `FoodCategory`
- `FoodAddon`
- `ShoppingCart`
- `Discount`
- `Transaction`
- `PaymentAgent`

## Attributes and Operations

### `Customer`
- ID: string
- Name: string
- Email: string
- FavoriteRestaurants: Array[Restaurant]
- FavoriteFood: Array[Food]
- DiscountCoupons: Array[Discount]
- ShoppingCart: ShoppingCart
- `addToFavorites(Restaurant.ID)`

### Session
- Token: string
- Customer: Customer
- `generateGuestCustomer() : Customer`

### ShoppingCart
- ID: string
- CustomerID: string
- Food: Array[Food]

### `Restaurant`
- ID: string
- Name: string
- Description: string
- Logo URL: string
- Address: string
- Categories: Array[RestaurantCategory]
- FoodCategories: Array[FoodCategory]
- Rating: int
- `searchMenuItems(string)`

### RestaurantCategory
- ID: string
- Name: String

### FoodCategory
- ID: string
- Restaurant
- Name: string
- Food: Array[Food]
- ProminentFood: Food
### Food
- ID: string
- CategoryID: string
- Name: string
- Description
- Cost: float
- Rating: int
- FoodAddon: Array[FoodAddon]

### FoodAddon
- ID: string
- FoodID: string
- Name: string
- Cost: float

### Discount
- ID: string
- Name: string
- Description: string
- Discount: float
- Type: string

### Transaction
- ID: string
- Customer: Customer
- Restaurant: Restaurant
- Food: Array[Food]
- DiscountCoupons: Array[Discount]
- Subtotal: float
- PaymentMethod: PaymentAgent

### PaymentAgent
- From payment gateway API
