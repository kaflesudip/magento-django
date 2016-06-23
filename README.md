# Magento to Django converter

Extract data from Magento to Django. Currently converts Magento products and users to Django fixtures.


## Installation

1. Clone the repository
2. Use Python 2 and install requirements using `pip install -r requirements.txt` from the base directory.
3. Run `jupyter-notebook` on terminal to test if its runnig correctly.

### Steps for extracting and loading products:

1. First export data from your Magento application. In admin page goto System -> Export. Select Product as entry Type and click continue.
2. Rename the downloaded file to `products.csv`.
3. Copy the file `products.csv` to the base directory.
4. Open `jupyter-notebook` and open `Extract products from magento.ipynb`. Run the program.
5. The required fixtures is saved as `fixtures.json` in your base directory.
6. Make sure that you have installed the Django ecommerce application correctly. Copy the fixture to `ecommerce/apps/catalogue/fixtures` directory in the Sample ecommerce site.
7. Install the fixture using `python manage.py loaddata ecommerce/apps/catalogue/fixtures/fixtures.json`.

### Steps for extracting and loading Users:

1. First export data from your Magento application. In admin page goto System -> Export. Select `Customers Main File` as entry Type and click continue.
2. Rename the downloaded file to `customers.csv`.
3. Copy the file `customers.csv` to the base directory.
4. Open `jupyter-notebook` and open `Extract Users.ipynb`. Run the program.
5. The required fixtures is saved as `user_fixtures.json` in your base directory.
6. Make sure that you have installed the Django ecommerce application correctly. Copy the fixture to `ecommerce/users/fixtures` directory in the Sample ecommerce site.
7. Install the fixture using `python manage.py loaddata ecommerce/users/fixtures/user_fixtures.json`

