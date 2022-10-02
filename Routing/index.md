# Routing
1) import {BrowserRouter as Router} from "react-router-dom"
2) Pack authentication app with Router
3) Now goes on Authentication App import {Routes,Route,Link} from "react-router-dom"
4) convert a tag into Link and href into to
5) set Routes for application 
    <Routes>
     <Route path="/discover" element={<DiscoverBooksScreen user={user}/>}/>
     <Routes><Route path="/discover" element={<BookScreen user={user}/>}/>
     <Routes><Route path="/discover" element={<NotFoundScreen/>}/>
    </Routes>
6) add Link to BookRow component ----> <Link to={`/book/${book.id}`}/>
7) then goes to notfoundscreen and give go to home link their (if no book found then user can easily come on home page with the help of link)
8) then goes to book.exercise import {useParams} from "react-router-dom"
         const {bookId}=useParams()
                                
