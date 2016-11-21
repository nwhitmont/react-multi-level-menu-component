# react-menu-component

## Purpose
The purpose of the project is to create reusable multilevel menu.

## Configuration
Basic use of the DatePicker can be described with:
```javascript
        <MenuList
          listClass={'context-menu'}
          itemClass={'context-menu-item'}
          triangleClassName={'context-menu-item-triangle'}
          position={{top: 50, left: 40}}
          clickItemCallback={this.clickItemCallback}
          show={true} items={items} />
```

## API

### listClass
Css class which will be applied to list container in menu

### itemClass

Css class which will be applied to item of  menu list

### triangleClassName

Css class which will be applied to svg triangle within nested menu item

### position 
Takes an object with to parameteres: top and left. Will be used to position menu on the page.

### clickItemCallback

Function which will be called when not a nested item will be clicked. Each click callback receives item name.

### show

Boolean which controls whether a menu should be shown.

### items 
An array of items with next structure:
```javascript
var items = [
  {
    text: 'Item 1',
    name: 'item-1'
  },
  {
    text: 'Item 2',
    name: 'item-2',
    items: [{
      name: 'sub-item-21',
      text: 'SubItem 21'
    }
  }
];
```
Where ``` text ``` will be used for visual representation of item and ```name ```  will be passed to each  ``` clickCallback ``` function.

Any ```  item ``` may have it's own ```  items ``` parameter, they will be rendered as a nested menu for an item. 