Multi Companies
===============

A centralized management environment allows you to select multiple companies simultaneously, and set
their specific warehouses, customers, equipment and contacts. It provides you the ability to
generate reports of aggregated figures without the need of switching interfaces, which facilitates
daily tasks and the overall management process.

Manage companies
----------------

Go to :menuselection:`Settings --> Manage Companies` and fill in the form with your companies’
information. If a *Parent Company* is selected, records are shared between the two companies.

.. image:: media/create_js_store_us.png
   :align: center
   :alt: Overview of a new company's form in Odoo

.. tip::
   Activate the :doc:`Developer mode <../../general/developer_mode/activate>` to choose a *Favicon*
   for each of your companies, and easily identify each of them by the browser tabs. Set your
   favicons’ files size to 16x16 or 32x32 pixels. JPG, PNG, GIF and ICO are extensions accepted.

   .. image:: media/favicon.png
      :align: center
      :height: 200
      :alt: View of a web browser and the favicon for a specific company chosen in Odoo

Switch between or select multiple companies by enabling their selection boxes to activate them. The
grayed company is the one which environment is in use. To switch environments, click on the
company’s name. In the example below, three companies are available for that user, two are
activated, and the environment in use is of *JS Store US*.

.. image:: media/multi_companies_menu_dashboard.png
   :align: center
   :alt: View of the companies menu through the main dashboard in Odoo

Data such as Products, Contacts, and Equipment can be shared or set to be shown for a specific
company only. To do so, on their forms, choose between:

- A blank field: the record is shared within *all* companies.
- Adding a company: the record is visible to users logged in to that specific company and its child
  companies.

.. image:: media/product_form_company.png
   :align: center
   :alt: View of a product's form emphasizing the company field in Odoo Sales

Multi-company access to employees
---------------------------------

Once companies are created, determine to which ones employees can have access to by managing
their :doc:`access rights <../odoo_basics/add_user>`.

.. image:: media/access_rights_multi_companies.png
   :align: center
   :alt: View of an user form emphasizing the multi companies field under the access rights tabs
         in Odoo

| If a user has multiple companies activated on his database and it is *editing* a record, the
  editing happens in the related company of the data/document.
| Example: if editing a sale order issued under JS Store US while working on the JS Store Belgium
  environment, the changes are applied under JS Store US (the company from which the sale order
  was issued).
| When *creating* a record, the company taken into account is:

- The current company (the one active) or,
- No company is set (on products and contacts’ forms for example) or,
- The company set is the one already linked to the document (the same has if you were editing a
  record).

Documents’ format
-----------------

To set documents' formats according to each company, activate and select the respective one and,
under Settings, click on *Configure Document Layout*.

.. image:: media/document_layout.png
   :align: center
   :alt: View of the settings page emphasizing the document layout field in Odoo

Inter-Company Transactions
--------------------------

First, make sure each one of your companies is properly set in relation to:

- :doc:`Chart of Accounts <../../accounting/overview/getting_started/chart_of_accounts>`
- :doc:`Taxes <../../accounting/fiscality/taxes/default_taxes>`
- :doc:`Fiscal Localizations <../../accounting/fiscal_localizations/overview/fiscal_localization_packages>`
- :doc:`Pricelists <../../sales/products_prices/prices/pricing>`
- :doc:`Warehouses <../../inventory/management/warehouses/warehouse_creation>`

Now, activate the *Inter-Company Transactions* option under *Settings*. With the respective company
activated and selected, choose if you would like operations between companies to be synchronized at
a invoice/bills level, or, synchronized at a sales/purchase orders level.

.. image:: media/inter_company_transactions.png
   :align: center
   :alt: View of the settings page emphasizing the inter company transaction field in Odoo

- **Synchronize invoice/bills**: generates a bill/invoice when a company confirms a bill/invoice for
  the selected company. On both environments *Fiscal Positions* and *Journal Entries* need to be
  set in order for the automated operation to happen.

  *Example:* an invoice posted on JS Store Belgium for JS Store US, automatically creates a vendor
  bill on the JS Store US from the JS Store Belgium.

.. image:: media/invoice_inter_company.png
   :align: center
   :alt: View of an invoice for JS Store US created on JS Store Belgium in Odoo

- **Synchronize sales/purchase order**: generates a drafted purchase/sales order using the selected
  company warehouse when a sales/purchase order is confirmed for the selected company. If instead of
  a drafted purchase/sales order you rather have it validated, enable *Automatic Validation*.

  *Example:* when a sale order for JS Store US is confirmed on JS Store Belgium, a purchase order
  on JS Store Belgium is automatically created (and confirmed if the *Automatic Validation* feature
  has activated).

.. note::
   Products have to be configured as *Can be sold*.

.. image:: media/purchase_order_inter_company.png
   :align: center
   :alt: View of the purchase created on JS Store US from JS Store Belgium in Odoo

.. tip::
   Remember to test all work-flows as an user other than the administrator.

.. seealso::
   - :doc:`../../accounting/others/multicurrencies/how_it_works`

.. LINK JOURNAL AND FISCAL POSITIONS DOCS ONCE AVAILABLE.