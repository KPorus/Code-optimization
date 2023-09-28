## Code optimization for large project in next Js ###

1. SSR VS CSR
=> SSR-> server side rendering
   CSR-> Client side rendering

   For an E-commerce site, SSR is best for showing data-related products.
   Cause say there are 1000 or more data and we are showing them in card
   In server-side rendering, at first, it will generate HTML and fetch data of 
   products from the server to the next JS server then show them. Here the HTML file will
   only generate one time and data will be fetched every time we click on that page.
   For generating an HTML page only one time, site performance increases.

   On the other hand, if we use CSR for showing data-related products, the site performance will
   drop cause for each data request the site will create html again and again.

   That's why SSR is better for e-commerce site product shows.

2. Image Optimization
=> Image Optimization is the most important part of increasing the site performance. If there is a large image in the site then it
   will trigger LCS warring. LCS means "Largest Contentful Paint". That's why we have to optimize the image. IN next js there
   is an Image tag that optimizes the image by default. Also, there is an npm package named Sharp which optimize image in production.

   For optimizing images we can use lazy loading. Lazy loading is active by default in next js. We can also prioritize the image load
   by using 'priority=true'

3. Dynamic Import
=> In The next JS it generates The HTML page only one time. Now say if there is a page in which there are 7 or more sections and with 
   an image then it will take more time to load a single page. For that case, we need to use dynamic import. By this we lazy 
   loading the component. Dynamic import is another amazing feature of the next JS.

4. Use of CSR
=> CSR-> Client-side rendering. We can use this CSR to handle user requests like checkout, number of quantity, or confirm order       
   requests. Cause in the next JS, it generates the HTML on build time if we build checkout/order pages then it can cause show 
   loading and create pressure on the next JS server. That's why we can use CSR for this type of case.