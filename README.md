# graphiQL-restaurantData
GraphQL restaurant Data - quey and mutations to  perform CRUD operations
run https://localhost:5500/graphQL
run mutations
mutation editrestaurants($idd: Int = 1, $name: String = "OLDO") {
  editrestaurant(id: $idd, name: $name) {
    name
    description
  }
}

mutation setrestaurants {
  setrestaurant(input: {
    id: 4
    name: "Granite",
    description: "American",
  }) {
    id
    name
    description
  }
}

mutation deleterestaurants($iid: Int = 2) {
  deleterestaurant(id: $iid) {
    ok
  }
}
query getrestaurant($iid: Int = 1) {
  restaurant(id: $iid){
    name
    description
    dishes {
      name
      price
    }
  }
}
query getrestaurants {
  restaurants {
    id
    name
    description
    dishes {
      name
      price
    }
  }
}


Which will manipulate the data accordingly.


Future Enhancements :
Now the newly created ids are null or input value which can be modifies to auto generated id value.
