## Proposal for mused-finds
Final Project Proposal — Mused Finds

## 1. The Three Ideas
- Mused Finds: An AI-powered web application for my friend who is building a startup called Mused basically she is building a platform that brings together carefully curated collections of unique clothing pieces from a wide range of brands. This would make it easier for people to discover distinctive fashion finds they might not come across otherwise. But she is overwhelmed and this would help her save and organize products she discovers across different websites into visual collections.
- The Intro Lab: An AI networking assistant for my friends who are currently applying for jobs, helping them write personalized outreach messages, organize contacts, and manage follow-ups.
- Weather Window: An AI travel assistant for my cousin who enjoys road trips, using weather data and personal preferences to recommend activities, hiking trails, and places to visit.


## Why not the other 2: 
- The Intro Lab: I actually really liked this idea because networking is something my friends and I are currently doing. However, I felt that simply generating outreach messages might be a bit too straightforward, and I wasn't sure what would make users consistently return to the application.
- Weather Window: I thought this could be useful, especially after planning my own road trip, but I felt that it was a bit too specific. It's something someone might use during a trip, rather than regularly throughout the year. 

I ultimately chose mused-finds because I see a real need for it, and I think my friend would genuinely use it frequently while building Mused.

## 3. What I Am Building
I'm building a sort of Pinterest-style web application that uses AI to automatically I'm building a web application that helps users organize all the products and unique finds they discover while browsing different websites, instead of keeping dozens of tabs open or saving scattered links in their notes. Users will simply paste a product URL, and the application will automatically retrieve its image, name, and price. AI will then categorize the item into a collection making it easy to keep track of everything they've discovered and find it again when they need it without having to search through so many tabs.

## 4. Who It Is For
I'm building this for my friend, who is currently developing Mused, a fashion platform similar to Revolve, but focused on bringing together carefully curated collections of unique and distinctive pieces from different brands. Her goal is to make it easier for people to discover clothing they wouldn't necessarily come across on traditional shopping websites.

When I was with her and seeing her develop this website, I noticed that she spends a lot of time discovering products across websites like Etsy, Depop, Vinted, Vestiaire Collective, 1stDibs, Instagram, and Zara. The problem is that all these links end up scattered across dozens of open tab it's super difficult to remember those unique pieces. I want to create one place where she can easily save, organize, and revisit all her finds as she builds her collections for Mused, without constantly having to search through endless tabs.

## 5. What the User Does
The user logs into the website and sees her saved products organized into visual boards, similar to Pinterest. When she discovers something she likes, she copies the product URL from the original website and pastes it into My Finds.
The application then attempts to automatically retrieve the product's name, price, and main image. AI identifies which category the product belongs to and adds it to the appropriate collection. She can browse through categories, open a saved product, and click the original link when she's ready to purchase it. There will also be an AI search feature where she can type something like Find the brown vintage boots I saved and the application searches her existing collection.

## 6. Data
The application will use Supabase for user authentication, database storage, and product images.
It will store:
- The user's account information.
- Product names, prices, categories, and original website URLs.
- One main image for each product.
- Saved collections organized by category.
From what I understood, product information will be retrieved from publicly accessible shopping webpages where possible. Then, A backend function will attempt to extract the information, and an AI model will categorize the items and help users search through their collections.
In principle, the database will allow her to access the same saved products from her phone or laptop.

## 7. Features
1. Automatic product saving: Paste a product URL and automatically retrieve its name, price, and main image where possible.
2. AI categorization: Automatically organize saved products into categories such as clothing, shoes, bags, accessories, and furniture.
3. Pinterest-style collections: Display saved products in visual boards that are easy to browse.
4. AI-powered search: Let the user describe a product in their own words and then find a matching piece from their saved collection.
5. Personal account and saved data: Allow the user to log in and access her collections across different devices, with manual entry available when extraction fails.

## 8. States and Their Tests
* Not logged in: Check that users cannot access saved collections without logging in.
* Empty collection: Check that a new user sees an empty collection with an option to add products.
* Valid URL: Paste a real product link and check that the correct image, name, and price appear.
* Invalid URL: Enter an incorrect link and check that an error message appears.
* Extraction failure: Check that users can manually add product information if automatic extraction fails.
* AI categorization: Save different products and check that AI places them in the correct categories.
* AI search: Search for a saved item using a description and check that the correct product appears.
* Saved data: Log out and back in to confirm that all products and collections are still saved.
* User testing: Have my friend test the live application and make at least one change based on her feedback.

## 9. What I do not know yet: 
 I am unsure whether my application can reliably extract and store product images from third-party platforms such as Depop, Etsy, and Vinted.. I did my first technical test, and instead of extracting, it generated a picture of the product. As I continue in this project, I would have to constantly test with different URLs to see if the real Depop listing will display in my application. If automatic extraction fails, users will be able to upload a product image manually. 