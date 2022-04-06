# Official User.com Userengage Methods Tag for Google Tag Manager

https://user.com/en/integrations/javascript/

##### Send data using Userengage methods

These methods let you trigger actions when specific scenario happens.



##### User.com | Implementation must be loaded to use Userengage methods


#### Methods available

- Send Event
- Send Product Event
- Update User


**Send Event**

Send event with your custom name and desired event attributes. Remember, create event attributes with specific data types before sending them over to User.com. 
To learn more about Events, read the article below.
https://docs.user.com/what-are-events-and-how-to-create-them/


**Send Product Event**

Using this method, you can trigger a product event on a specific action. To learn more about product events, read the article below.
https://docs.user.com/how-to-create-product-events/


**Update User**

Using this method, you can update user attributes as well. However, it won't create a pageHit. Not every attribute can be changed with this method. Please, check the attributes' list in the article below:
https://docs.user.com/user-data-list-of-articles/


### Configuration

#### Send Event

##### Required configuration data

- **Event Name**
    - Choose any appropriate Name for your Event
    - Event does not have to be created before using it

##### Optional attributes

- **Event Attributes**
    - Pass data to add attributes to the Event
    - Provide standardized attribute names without blank characters, i.e. Do not use First Name, use first_name instead
    - Undefined values will not be passed


#### Send Product Event

##### Required configuration data

- **Product Event Type**
    - Choose Product Event Type corresponding with an action you want to track

- **Data Type**
    - Choose Type based on the data format used
    - Use **Single Product Event** for Object:
        - {
            name: "Coffee Maker Cimbali",
            id: "712016",
            price: "749",
            brand: "Cimbali",
            variant: "Steel",
            variant_id: "388954"
        }
    - Pass Product ID

    - Use **Product Event from Array** for Array of Products:
        - 'products': [
            {
                name: "Coffee Maker Cimbali",
                id: "712016",
                price: "749",
                brand: "Cimbali",
                variant: "Steel",
                variant_id: "388954"
             }
            ]

##### Optional product attributes

 - **Single Product Attributes**
    - Attributes configuration available only when this option is choosed
    - Pass data to configure standard and custom Product attributes
    - Provide standardized attribute names without blank characters, i.e. Do not use First Name, use first_name instead
    - Undefined values will not be passed

##### Optional data structure

- **Product Event from Array**
    - Path configuration available only when this option is choosed
    - Configure fields if you have different data structure than standarized:
        - {
            name: "Coffee Maker Cimbali",
            id: "712016" }
    - I.e use it when you are using item_id instead of id.


#### Update User

##### Optional User attributes

- Pass data to update standard and custom User attributes.
- Provide standardized User attributes without blank characters, i.e. Do not use First Name, use first_name instead.


##### Optional configuration data

- **Console Logs**
    - Select to enable debug console logs.
    - Selection will enable logs in both Preview and Published containers