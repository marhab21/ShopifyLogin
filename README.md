# ShopifyLogin
Multipass encryption in pure Javascript using Stanford Javascript Crypto Library, as modified by Sampath Dimmala.
Using Cody Smith's nodejs port as a guide. 

Here is the embedded javascript from the html file:

<script type="module" src="./multiclass.js"></script> 
<script type="text/javascript" src="sjcl.js"></script> 


<script type="module">

  import ShopifyMultipass from './multiclass.js'
 
  // Construct the Multipassify encoder
  var multipass = new ShopifyMultipass("multipass_key");

  // Create your customer data hash
  var customerData = { email: 'user@email.com' };

  // Generate a Shopify multipass URL to your shop
  var url = multipass.generateUrl(customerData, "yourstore.myshopify.com");
  // For debugging purposes:
  console.log("URL: %s", url);


  // Generates a URL like:  https://yourstorename.myshopify.com/account/login/multipass/<MULTIPASS-TOKEN>

</script>
