---
layout: default
---

# Auto screen refresh after adding stock using Ajax

In this tip we are looking how to show new stock items in the stock list using Ajax. No screen refresh or reload needed. This tip assume that you already have an Ajax call to show your stock on the screen and an Ajax call that adds new stock. After adding new stock you currently have to refresh your screen to see the added item. This tip will show you how to fix that.

Create a function that containts the code that show all you stock items onto the screen.

```javascript
function showStock(){
  ajaxGetCall("/api/stock/all", function(data){
    stockListElemenet.innerHTML = stockTemplate(data);
  });
}
//show all the stock
showStock();
```

To refresh the stock list call the `showStock` function in the add new stocks's Ajax call callback.

```javascript
function addStock(stockItem){
  ajaxPortCall("/api/stock/add", stockData, function(){
    // now your screen should refresh automatically.
    showStock();
  });
}
```

Now any new stock added will be displayed onto your screen immediately.

The general principle here is that after data changed on the server you can update a section of a screen, by doing a Ajax call to get the fresh data and then re-render the section using the DOM.
