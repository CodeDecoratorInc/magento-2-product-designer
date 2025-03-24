# Magento 2 Product Designer Extension

## Introduction
The **Magento 2 Product Designer** extension by CodeDecorator empowers customers to personalize their products with custom text, images, and clipart. This powerful **Web to Print** solution enhances user engagement and boosts conversions by offering a seamless customization experience. 

## How It Works
The **Magento 2 Product Designer** extension integrates with your store, allowing users to personalize products directly on the product page. Customers can add custom text, change fonts, select predefined clipart, and upload their images. Admins can configure settings such as personalization charges, default fonts, and available colors from the backend.

## Key Features
- **Live Product Personalization** – Customers can see real-time changes while customizing their products.
- **Clipart & Custom Font Support** – Upload clipart images and custom fonts for unique personalization.
- **Restricted Personalization Area** – Define specific areas where customization is allowed.
- **Download Printable Designs** – Customers and admins can download high-resolution printable images.

## Custom Font Upload
Admins can upload custom fonts by navigating to **Personalized Products > Manage Fonts** and adding a new font.

## Clipart & Category Management
Admins can upload multiple clipart images and assign them to categories from **Personalized Products > Manage Cliparts**.

## Extension Installation
To install the **Magento 2 Product Designer** extension, use Composer, a powerful dependency management tool.

### Step 1: Install the extension using Composer
```bash
composer require codedecorator/magento2-product-designer
```
For a specific version:
```bash
composer require codedecorator/magento2-product-designer:<version>
```
*Note:* You may need authentication keys from the vendor or Magento Marketplace.

### Step 2: Run Magento commands
```bash
php bin/magento setup:upgrade
php bin/magento setup:di:compile
php bin/magento setup:static-content:deploy -f
php bin/magento cache:flush
```

## How to Configure Magento 2 Product Designer
After installation, follow these steps to configure the extension.

Once after successful installation of our extension, you will need to enable the extension from Magento2 admin. Following steps will guide for the same

1. Login to your Magento store admin  
2. Click on the **Codedecorator** Extension Menu
   
![img1](https://github.com/user-attachments/assets/43565ba5-de58-4191-a80a-46f43b056f3f)

3. Click on the configuration.

![img2](https://github.com/user-attachments/assets/54ada604-2ee5-4c5a-87f6-b2c77efe1e10)

4. Set the required general configuration shown in the image below.

![img3](https://github.com/user-attachments/assets/1f9a2318-3d26-4828-b6d7-57edb6cf3126)

**Enabled:-** Set Yes to Enabled module dropdown to activate the module for frontend.

**Note:-** When enable Personalization extension, Please install Imagick library on your
server.

**Personalization Require: -** If the select “Yes” Then personalization require for Product.

**Allow Add To Cart :-** If the select “Yes” then customer can direct add to cart product from
home or category page.

**Note :-** This field only shows when the “Personalization Require” field value is“No”.

**Personalized charge:-** Set the price for personalization. Product price + Price will be
added when customer buys product with personalization on frontend side.

**Email Template:-** Select Email Template For the Personalized Orders.

5. Set required configuration for the text shown in below configuration.

![img4](https://github.com/user-attachments/assets/50ede7e2-0f07-459a-b83a-55f4a5d8b05c)

If you set show palette set to YES then it will show only predefined colors which you have
set in the 3rd configuration field called “Text Color” and if you set it NO then it will show a
colorpicker with predefined color.

![image20](https://github.com/user-attachments/assets/11445007-8100-4561-bdf0-a4deb6bb6472)

6. Show predefined color on frontend and set the default color when customer first enters the
text on product image.

![img5](https://github.com/user-attachments/assets/97f57098-4917-4703-978f-8e0a16d6fc43)

***How to upload custom Font***
To upload a custom font for **personalization, click on Personalized Products Menu ->
“Manage Fonts”.**

![image15](https://github.com/user-attachments/assets/d5d36514-cc69-44b9-9aaf-67e47c117f8c)

After clicking on **“Manage Fonts”**, it will redirect to font grid where you will be able to see
the button called **“Add New Fonts”**.

![image9](https://github.com/user-attachments/assets/c3151ad8-f204-4ca4-b2c3-0c540dd37dfc)

Give the proper font name and upload the woff file of your custom font. Make status
**“Enabled”** and **Save** the font.

![image11](https://github.com/user-attachments/assets/28cc2da8-0afd-4913-852c-c8b485d02754)

**How to create Clipart and its Category**

Admin will need to first upload Clipart Images and assign those images to category. To
create clipart,
navigate to Personalized Products Menu -> **“Manage Cliparts”** and click on the **“Add New
Clipart”.**

![image22](https://github.com/user-attachments/assets/f5efac2f-dab2-4813-a64e-074331d690ee)

Admin can upload as many clipart images as they want. Once after uploading the clipart
images, the admin needs to create a new category and assign the created clipart.
To create new category for clipart , go to Personalized Products Menu -> **“Manage
Category”** and click on the **“Add New Category”**

![image24](https://github.com/user-attachments/assets/7315a10e-135b-4ada-9442-caaca12ee7d9)

Provide the name to Category and set the status **“Enabled”** of the category in **General Tab.**
Click on the 2 nd tab called **“Cliparts”** and assign all the clipart images which you need to
assign to the category.

![image31](https://github.com/user-attachments/assets/1e8448ad-0f22-4961-913a-0c794fab8d11)

![image28](https://github.com/user-attachments/assets/fdf8c17f-bd2e-47c2-8bad-5e6680265053)

After assigning the **“Cliparts”,** click on the 3rd tab named **“Products”** and select all the
products in which you want to assign this clipart category and save the category. If you don't
assign a product to a category then it wont show on the product page.

![image17](https://github.com/user-attachments/assets/5bcff7c8-0940-4844-8d38-cdaba4fdc0f9)

If no category is assigned to the product then **“Clipart Tab”** on the front side won't display.

**Product configuration**

Once global configuration is done, the admin needs to enable the extension product wise.
There are two ways to enable personalized products.

***1. Without Restricted Area.***

***2. With a Restricted Area.***

**Enable Product Without Restricted Area**

Search for the product in which you want to enable the personalization and click on edit
action link.

![image4](https://github.com/user-attachments/assets/36c27b33-494c-485a-8179-d38430932c7b)

Set **“Enable Personalization”** to **YES** which will enable personalization on the product
page. Set price for personalization, fix cost for product. If you don’t set a price then it will
consider the global configuration price cost.

![image33](https://github.com/user-attachments/assets/8173dedb-8c7c-4aec-90ab-c1aed0d93765)

**Note:** When you just enable the personalization without setting any area on the product
image then it will consider the entire product image as a full personalization area.

**Product image without setting area.**

![image18](https://github.com/user-attachments/assets/a37bb7aa-c301-45f2-a708-c8d9cd7c893a)

**Enable Product Restricted Area**

When you don't want your customer to draw anything on the entire image then you can
create a restricted area on the product image so the customer can not add anything outside
the restricted area.

Please follow the given steps to draw a restricted area on product image.

***1. Click on the pencil button available on the product image.***

![image36](https://github.com/user-attachments/assets/4b66fd41-be26-466e-a140-2f21866804ed)

***2. Drag and draw the rectangle area on the product image.***

![image19](https://github.com/user-attachments/assets/babd6a8d-1059-4da7-ba98-0a84680b5707)

Once you are done with drawing restricted area, click on the save area button.

![image5](https://github.com/user-attachments/assets/f2448c35-1374-4c1b-b612-33334fcac71d)

**Personalized Product on product page.**

Customers will be able to see options to select the Normal or Personalized , once Admin
enables the personalization on the product page.

![image21](https://github.com/user-attachments/assets/06d69880-1910-48fe-b20b-c651c6d34036)

When customer click on the Personalized option , it will show various option to customer to
**“Add Text”**,**“Add Image”* and “Select Clipart Image”(predefined images).

**ADD TEXT**

In “Add Text” users will be able to add any text on product image after adding text in
textarea and click on the “Add Text” button.

Users will be able to drag and move added text on product images. Users also can change
the font family of the text, color and all font styling after selecting the text. Users just need
to click the added text to select.

![image1](https://github.com/user-attachments/assets/d8231c3f-a222-4d2a-931b-353751b30928)

![image7](https://github.com/user-attachments/assets/37417163-f970-40ee-98c6-24cf71c35730)

Using the “Upload image” , customers can upload any custom image they want to add in
personalization while using clipart they will be able to add predefined images given by
admin.

![image6](https://github.com/user-attachments/assets/a179548b-5644-46d1-8de4-2ba90b9b3a0a)

**Personalized Product Preview on Mini Cart**

Once a customer is done with personalization and adds the product into cart, they can
preview the final customization done over product image on minicart.

![image8](https://github.com/user-attachments/assets/b5f125d7-c662-4ad7-8525-f2d1085cb6e6)

![image10](https://github.com/user-attachments/assets/edb19b0c-8b6b-4428-93b5-3f00cc7f48d2)

**Personalized Product Preview on Cart**

Once a customer is done with personalization and adds the product into cart, they can
preview the final customization done over product image on cart page. Users can click on
the generated image to preview the product image in the popup.

![image2](https://github.com/user-attachments/assets/6bcb9df3-4870-474a-86d9-0617390078ec)

**Image preview in customer account**

Customers can preview the customized version of the image in their account under the sale
order view page.

![image13](https://github.com/user-attachments/assets/0809f259-485b-45fe-93cc-8b269dc14993)
 
**Download the final printable image.**
***1. Find the personalized order from sale order grid***

![image16](https://github.com/user-attachments/assets/c355c26f-61a9-4fe0-8854-66895278018c)

***2. View an order and click on the download link to download all the personalized
images.***

![image12](https://github.com/user-attachments/assets/837ccf58-cab6-451c-85f1-50c48bec565b)

## Download Our [Magento 2 Product Designer](https://codedecorator.com/magento-2-product-designer.html) Extension

