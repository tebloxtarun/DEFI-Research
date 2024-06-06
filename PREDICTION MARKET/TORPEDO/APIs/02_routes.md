This table organizes the HTTP methods, routes, and the corresponding action in the controller.

### Tournament API Routes

| HTTP Method | Route                        | Controller Action     |
|-------------|------------------------------|-----------------------|
| POST        | /tournaments                 | tournaments#create    |
| PATCH       | /tournaments/:id             | tournaments#update    |
| PUT         | /tournaments/:id             | tournaments#update    |
| DELETE      | /tournaments/:id             | tournaments#destroy   |
| POST        | /tournaments/:id/move_up     | tournaments#move_up   |
| POST        | /tournaments/:id/move_down   | tournaments#move_down |

### Tournament Group API Routes

| HTTP Method | Route                                  | Controller Action               |
|-------------|----------------------------------------|---------------------------------|
| POST        | /tournament_groups                     | tournament_groups#create        |
| PATCH       | /tournament_groups/:id                 | tournament_groups#update        |
| PUT         | /tournament_groups/:id                 | tournament_groups#update        |
| DELETE      | /tournament_groups/:id                 | tournament_groups#destroy       |
| POST        | /tournament_groups/:id/move_up         | tournament_groups#move_up       |
| POST        | /tournament_groups/:id/move_down       | tournament_groups#move_down     |

### Markets API Routes

| HTTP Method | Route                     | Controller Action    |
|-------------|---------------------------|----------------------|
| GET         | /markets                  | api/markets#index    |
| GET         | /markets/:id              | api/markets#show     |
| POST        | /markets                  | api/markets#create   |
| POST        | /markets/:id/reload       | api/markets#reload   |
| GET         | /markets/:id/feed         | api/markets#feed     |

### Portfolios API Routes

| HTTP Method | Route                             | Controller Action         |
|-------------|-----------------------------------|---------------------------|
| GET         | /portfolios/:id                   | api/portfolios#show       |
| POST        | /portfolios/:id/reload            | api/portfolios#reload     |
| GET         | /portfolios/:id/feed              | api/portfolios#feed       |

