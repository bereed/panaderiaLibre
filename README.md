Panaderia Libre Viewer

Welcome to the Panaderia Libre Viewer! This is a lightweight, static web application designed to display recipes and products for formulas, mixtures, and ready-to-make products. It supports dynamically loading JSON files containing metadata, ingredients, and instructions for various recipes.


---

Features

Dynamic JSON Rendering:

View recipes or products by providing a JSON file URL in the query string.

Displays metadata, ingredients, instructions, and more.


Support for Primary and Sort Keys:

Displays PK (Primary Key) and SK (Sort Key) fields if present in the JSON.


Directory Listings:

Links to browse formulas, products, and mixtures when no specific JSON file is provided.


Static and Lightweight:

Fully functional with GitHub Pages or any static hosting service.




---

Usage

1. Clone the Repository:

git clone https://github.com/bereed/panaderiaLibre.git
cd panaderiaLibre


2. Open the Viewer Locally:

Open index.html in your browser to explore the viewer.



3. Load Specific JSON Files:

Append a ?formula= query string to the URL with the JSON file path.

Example:

file:///path/to/index.html?formula=https://bereed.github.io/panaderiaLibre/products/buttermilk-sourdough-products.json



4. Explore Categories:

Without a ?formula query, the viewer will list available directories (e.g., Formulas, Products, Mixtures).





---

JSON Structure

The viewer expects the following JSON structure:

Top-Level Keys

pk: Primary Key (e.g., prod-collection-001).

sk: Sort Key (e.g., buttermilk-sourdough).

metadata: Contains the name, description, version, and tags.

products or ingredients: Array of items with detailed information.

instructions: Steps for preparation (optional).


Example JSON

{
  "pk": "prod-collection-001",
  "sk": "buttermilk-sourdough",
  "metadata": {
    "product_name": "Buttermilk Sourdough Products",
    "version": "1.0.0",
    "description": "A soft, tangy sourdough product available in multiple sizes."
  },
  "products": [
    {
      "id": "prod-001",
      "type": "Regular Loaf",
      "weight_grams": 500,
      "price": 6.99,
      "bulk_discount": { "min_quantity": 5, "price_per_unit": 5.99 }
    }
  ]
}


---

Hosting

To host the viewer, you can use GitHub Pages or any static hosting platform.

1. Enable GitHub Pages:

Go to the repository settings on GitHub.

Enable GitHub Pages under the "Pages" section.



2. Access the Viewer:

Visit: https://<your-username>.github.io/panaderiaLibre/index.html.



3. Test JSON Files:

Use a query string to load JSON:

https://<your-username>.github.io/panaderiaLibre/index.html?formula=https://<your-username>.github.io/panaderiaLibre/products/buttermilk-sourdough-products.json





---

Contributing

Contributions are welcome! To contribute:

1. Fork the repository.


2. Create a new branch for your feature or bug fix.


3. Submit a pull request with a detailed explanation of your changes.




---

License

This project is licensed under the MIT License. See the LICENSE file for details.


---

Feedback

If you encounter issues or have suggestions, feel free to open an issue in the repository.

Happy baking with Panaderia Libre Viewer! 🥖
