#H1 Telecom APIs
This challenge should take you ~30 minutes of time (let's keep it simple) and isn't related to any particular language, you can even implement it in pseudo-code, as we're more interested in your software design skills rather than knowing if you know all the array_* functions.

Background
We are a TeleCom operator.

In our DB, we are starting to store phone numbers associated to customers (1 customer : N phone numbers) and we will provide an API to modify them.

We need 3 APIs:

get all phone numbers
get all phone numbers of a single customer
activate a phone number
Challenge
Provide us the API endpoints (and HTTP methods) used to implement those 3 APIs.

For each endpoint, describe a controller method (you decide which dependencies you can use) that implements the API.

Example
API description:

retrieve a list of dogs

API endpoint:

GET example.org/api/dogs

API implementation:

function getDogs($req, $res, $db) {
    $dogs = $db->getAllDogs()->toArray();
    $res->setData($dogs);

    return $res;
}
Another example could be:

API description:

retrieve a list of dogs

API endpoint:

GET api.example.org/v1/dogs

API implementation:

function getDogs(list $criteria, $dogRepository) {
    $dogs = $dogRepository->filterBy($criteria);

    return httpResponse::create($dogs);
}
Feel free to use the design that you think is best! 
