# Cache Management 
## Caching is a technique that helps us to stores a copy of a given resource into our browser and serves it back when requested.
## We can use the following approach in for to store single data into cache in ReactJS. We can cache some data into the browser and use it in our application whenever needed.

## useMutation
### useMutation will track the state of the mutation
### used for easily making mutations 

### Arguments:-
useMutation(mutationFn, {
   mutationKey,
   onError,
   onMutate,
   onSettled,
   onSuccess,
   retry,
   retryDelay,
   useErrorBoundary,
   meta,
 })

example:- const [create]= useMutation(
            ({ bookId }) => client("list-item", { data: { bookId }, token: user.token }),
             {onSettled:()=>queryCache.invalidateQueries('list-items')}
 )

https://react-query-v2.tanstack.com/reference/useQuery

## useQuery
### custom hook to fetch data
### also caching data after initial fetch 
### re-fetching data in the background etc

example:- const {data:listItems}=useQuery({
                    queryKey:"list-items",
                     queryfn:()=>client('list-items',{token:user.token}).then(data=>data.listItems)
})


### take two-three argument:-
1. query key or array  string | unknown[]
2. function that return promise 
3. enabled (boolen value only)

###Return:-
1. return promise that fulfills with a query result when the query succeeds or fails.

## queryCache
### it store all the data, meta information & state of queries it contains.
### we will not interact with the query cache directly 


# Exercise

## How to use useMutation hook? What are it's argument?

- why it is used ?
- What does it return?
- How to call api here?
- How to pass data and token into client fxn ?
- How to wireup this function onClick?
- What does function return i.e first argument of useMutation?

## how to use useQuery hook? its argument?
- why it's used?
- what it return?

## what queryCache do?
