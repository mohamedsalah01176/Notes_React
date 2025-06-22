# Notes_React// importants
    - npx create-react-app myproject || npm create vite@latest (recommended) => to create project react

    - npm => node packege manager
    - npx => node packege execute => do execute packege at computer with install it at your computer


// helpers
    - NavLink tag put class active on button
    - axios support every browser opposite fetch
    - We use usehooks at top level of function component

1- babel => convert ES6 to old javascript
2- webback => do minmize for folder, romove white space

3- angular(18) => 2009 (Google) , react(19) => 2013 (facebook)

4- deal with virtuar dom is best at preformance

5- when you do update (Reconcilation process) => engine (Fiber engine) will do create new virture dom and compare (Diffing Algorithm) it with virture dom and will applay it at real dom

6- Diffing Algorith 
    - deep comparison => engin compare referance (tags) and content, O(n)^3
    - shallow comparison =>  engin compare referance (tags) only, O(2)

7- react work at shallow comparison => because it best at preformance

8- Function Componenet  (recommended)
    - it has retun function to data
    - it has hooks
    - it is light at machine


8- Class Componenet 
    - it has render function to retun data
    - we must exdent from Componenet (react)
    - it is havy at machine


9- life cycle methods
    - mounting
        -- contractor => put initail data, we can not call api because it work when do change
        -- render => to retun html tags , we can not call api because it work when do change and if data used in html it will be error
        -- componenetDidMount => it work after page loaded, we can call api
    - updqting
        -- ShouldComponentUpdate => it call when check update then call Render method
        -- ComponenetDidUpdate => it call when did update, it use to do interaction for user => if you use useState in this menthod will occur infinite loop
    - unMounting
        - ComponenetWillUnMount => to clean up memory

10- trigger update 
    - state
    - props
    - ForceUpdete()
    - relation parent child
        -- useless Rerender
            1- ShouldComponentUpdate(nextProps,nextState)
            2- pureComponenet()

11- put images in assets VS public
    - assets
        -- we must do import for images
        -- webBack do optomize for image 
    - public
        -- we import by "/image.png"
        --  do not optomize for image 

12- jsx =>javascript xml

13- useState() hook => it replace constractor 
    - we use it to rerender Componenet 
    -  we when use it the variable do not return to initial variable when rerender
14- any code before return => it replace render

15- useEffect => we can make one or more useeffect
	- it replace life cycle for class
    - If you use useState in updating useEffect you will go at infinite loop
    - To provide useEffect to render at first time put if condition it
    - we call api at it To improve user experience and put spinner
	- useEffect(()=>{}) => render when occur any change (it is bad)      (componenetDidUpdate)      
	- useEffect(()=>{},[]) => render at once time                        (componenetDidMount)
	- useEffect(()=>{},[counter]) => render when occur changeon counter
16- methods at function componenet => it replace (shouldcomponenetUpdate)

17- cleanup => it replace (ComponenetWillUnMount)
	-useEffect(()=>{return ()=>{logic}},)

18- React Quary 
    - it is state management Servier (remote) state mengement , store and fetch data
    - put data in catch

19- Redux => local state mengement and use fetch to get data
