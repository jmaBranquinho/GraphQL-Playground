#How to replay it

Use npm install to get all the required packages that I had previously removed.
Use the command "npm run dev:server" on one console to start the graphql server.
Use the command "npm run json:server" on another console to start the json server that will provide the data.
By default the json server will run on port 3000 of the localserver while the graphql server will run on 4000.


Use the following link to access the graphiql route and to interact with the data: http://localhost:4000/graphql


All the CRUD operations/mutations are listed bellow:
- addCustomer
- deleteCustomer
- editCustomer


Examples:

-Query:

customer(id:"rytP7hhUW") {
  name,
  email,
  age
}

-Create:

mutation {
  addCustomer(name: "Bob", email: "Bob@Burger.com", age:33){
    id
  }
}

-Edit:

mutation {
  editCustomer(id:"rytP7hhUW", name:"Harry Potter"){
    id,
    name
  }
}

-Delete:

mutation {
  deleteCustomer(id:"rytP7hhUW"){}
}
