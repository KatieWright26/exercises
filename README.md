# Exercises

### Box Model

The box model refers to the box that each piece of content is wrapped in. This box contains several properties:
1. Content: where text, a link or image lives.
2. Padding: space between the content at the edge of the box. Background colors apply to the padding space.
3. Border: This wraps around the outside of the box and around the edge of any padding or content.
4. Margin: sits around all three inner layers and provides space between its box, and other box models.

Any width or height that is applied via CSS, is only applied the the content section of the model. Hovering over this element in the browser dev tools will display the _total_ width of the element, e.g. 

```
.myContent {
    width: 100px;
    height: 50px;
    padding: 40px 20px;
    margin: 20px;
    border: 5px solid purple;
}
```
Dimensions: 190px x 180px


### JS
```
const sales = [
{ itemSold: 'Football', price: 19.99, dateSold: '2018-04-07', id: 'j_123' },
{ itemSold: 'Trainers', price: 159.95, dateSold: '2018-03-02', id: 't_acds1' },
{ itemSold: 'Cricket bat', price: 204.97, dateSold: '2018-04-05', id: 'j_456'},
{ itemSold: 'Rugby ball', price: 30.00, dateSold: '2017-04-22', id: 't_acds3' },
{ itemSold: 'Hockey stick', price: 54.95, dateSold: '2017-03-19', id: 'j_999' }]
```
1. Sum of prices:
```
sales.reduce((total, sale) =>  sale.price += total, 0);
```
2. Items sold in 2017: 
```
sales.filter(sale => {
    const convertToDate = new Date(sale.dateSold);
    return convertToDate.getFullYear() === 2017;
});
```
3. Sort items sold: 
```
sales.map(sale => sale.itemSold).sort();
```
4. Find sale with ID: 
```
const findSaleById = (id) => sales.filter(sale => sale.id === id);
```

Layout exercise notes:

- All written in pure CSS
- Used media queries to impliment mobile first styles.
- Used a checkbox with pure CSS to impliment a sliding sidebar for narrow screen views.
- Used [WebAIM](https://webaim.org/resources/contrastchecker/) to ensure colours pass WCAG standards.
- 