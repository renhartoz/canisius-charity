
# Canisius Charity

Seat ticketing system


## API Reference

#### Get user's seats

```https
  GET /api/user/<user_email>
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `user_email` | `string` | **Required**. Email of the user to fetch owned seats for |

#### Get seat details

```https
  GET /api/seat/<seat_id>
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `seat_id` | `string` | **Required**. Id of seat to fetch |

#### Update seat owner

```https
  POST /api/seat/<seat_id>/post
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `seat_id` | `string` | **Required**. Id of seat to update |
| `owner_id`| `string` | **Required (in JSON Body)**. The ID/Email of the new owner |

#### Update seat order status

```https
  POST /api/seat/<seat_id>/is_order
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `seat_id` | `string` | **Required**. Id of seat to update |
| `orderStatus`| `boolean`| **Required (in JSON Body)**. The new order status |

#### Get all seats

```https
  GET /api/seats
```

No parameters required. Returns a list of all seats.

#### Get user by ID/Transaction ID

```https
  GET /api/user/<transaction_id>
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `transaction_id`| `string` | **Required**. ID used to identify the user |

#### Create or Update User

```https
  PUT /api/user/put
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `int`    | **Required (in JSON Body)**. User ID |
| `username`| `string` | **Required (in JSON Body)**. Username |
| `email`   | `string` | **Required (in JSON Body)**. User Email |
| `owned_seat`| `string`| **Required (in JSON Body)**. Seats owned |
| `amount`  | `int`    | **Required (in JSON Body)**. User balance/amount |

#### Get all users

```https
  GET /api/users
```

No parameters required. Returns a list of all users.

#### Process Transaction

```https
  POST /api/transaction/<user_email>
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `user_email` | `string` | **Required**. The email of the user making the transaction |
| `last_transaction`| `array` | **Required (in JSON Body)**. List of seat IDs to purchase |

#### Generate Payment Token

```https
  POST /api/tokenizer/<user_email>
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `user_email` | `string` | **Required**. The email of the user |
| `price`   | `int`    | **Required (in JSON Body)**. Price of the item |
| `id`      | `string` | **Required (in JSON Body)**. Item ID/Name |
| `first_name`| `string`| **Required (in JSON Body)**. User first name |
| `last_name`| `string` | **Required (in JSON Body)**. User last name |
| `email`   | `string` | **Required (in JSON Body)**. User email for billing |
## Acknowledgements

 - [Awesome Readme Templates](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)
 - [Awesome README](https://github.com/matiassingers/awesome-readme)
 - [How to write a Good readme](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)


## Appendix

This application is currently in beta due to a recent migration from CRA to Vite.

## Authors

- [@renhartoz](https://www.github.com/renhartoz)

## Assistance
- [@tokinohana](https://www.github.com/tokinohana)


