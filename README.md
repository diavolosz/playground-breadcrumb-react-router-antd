simple react router


In the RouteLink.js, it has all the item that is clickable and will direct to the new "route path". some will direct to an inner path such as those that are called innerNews.

when click, the route on the webpage will be updated. This trigger the BreadCrumb component to perform its function to render the correct crumbs

the BreadCrumb component in BreadCrumb.js has a function called BreadCrumbView does a few things 
  1) obtain the current route path from the webpage link (line 18)
  2) split the path into an array of crumbs (ine 19)
  3) Loop through the array of crumbs and selectively render the crumb in the order depending on whether the crumb is the first item, last item, or the items inbetween. 
  NOTE:
    - if the crumb is the first crumb () => render crumb with link that links to the first crumb (basically the default page) 
    - if crumb is the crumbs inbetween => render those crumbs with the link to the crumb 
    - if crumb is the last crumb => render its crumb name but without any link 

    e.g. 
      path = /Home/news/innerNews1
      pathArr = ['Home', 'News', 'innerNews1']
      crumb: Home / news / innerNews1

      Home is a link (will direct back to '/Home)
      news is a link (will direct back to '/Home/news')
      innerNews1 is NOT a link

  4) BreadCrumbView function will return a <div>. Therefore, we need to return this <div> to properly render the BreadCrumb component (line 56) 
  
        
if you already have an array of crumbs similar to line19, You ony need to render the crumb proper using this BreadCrumb component. Hope this hepls ! :)
