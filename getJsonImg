//This function gets the json data from an ajax request and then puts them into the scene
function getJsonImg(path) {

    //count the item name starting from 1      
    var itemCount = 1;

//Ajax request to dynamically pull data from server without refreshing the webpage
        $.ajax({
  dataType: "json",
  url: path,
  success: function(data) {
    $.each(data, function() {
        
//run through the received Json data and replace the existing elements with the new data by looping through and assigning the number (itemcount)
//based on the item.
  $.each(this, function(k, value) {
      
    console.log("before" + itemCount);
//Selects the item with the name property and then finds the original item in the html doc and replaces it with the new data
//It's important to keep the attributes that the text previously has in order for the replacement to go smoothly
    if (k === "name") {
        document.querySelector('#name' + itemCount +' ').setAttribute('text', 'color:black; opacity:1; width:3.5; align:center; value:'+ value + ';');
    }

    else if (k === "price") {
        document.querySelector('#price' + itemCount +' ').setAttribute('text', 'color:black; opacity:1; width:3.5; align:center; value:'+ value + ';');
    }

    else {

        document.querySelector('#img' + itemCount +' ').setAttribute('src', 'vr/img/'+ value);
            console.log("after" + itemCount);
            //This lets you know the item was successfully imported and the next one is coming up
            itemCount++;
    }

  });

  
