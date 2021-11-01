# SubQuery - Account Balance


The balance of the subquery - account is an example of displaying the balances of all accounts in the Polkadot network.
```

## Indexing and Query

#### Run required systems in docker


Under the project directory run following command:

```
docker-compose pull && docker-compose up
```
#### Query the project

Open your browser and head to `http://localhost:3000`.

Finally, you should see a GraphQL playground is showing in the explorer and the schemas that ready to query.

For the `subql-account-balance` project, you can try to query with the following code to get a taste of how it works.

````graphql
{
  query{
    accounts(first:10 orderBy:BALANCE_DESC){
      nodes{
        account,
        balance,
      }
    }
  }
}
````
