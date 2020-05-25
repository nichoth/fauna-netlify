# faunadb + netlify + ecommerce stuff

https://docs.fauna.com/fauna/current/integrations/netlify.html

https://docs.fauna.com/fauna/current/tutorials/ecommerce.html

```
npm i netlify-cli -g
cd my_project
netlify init
netlify addons:create fauna
netlify addons:auth fauna
```

Install the FaunaDB Shell on your computer.

```
npm i -D fauna-shell
fauna cloud-login
```

Need to make a key on the fauna dashboard > security website for the `cloud-login` command.

```
fauna create-database ecommerce-tutorial
fauna shell ecommerce-tutorial
```

Setup the database
```
fauna shell ecommerce-tutorial
CreateCollection({name: "warehouses"});
CreateCollection({name: "products"});
CreateCollection({name: "customers"});
CreateCollection({name: "orders"});
```

## create a function

Run the following query in the shell for creating the submit_order function:

[see docs](https://docs.fauna.com/fauna/current/tutorials/ecommerce.html#function)

## Submit an order
[see docs](https://docs.fauna.com/fauna/current/tutorials/ecommerce.html#submit-plenty)

We should also see that the products' quantities have been decreased accordingly. 


