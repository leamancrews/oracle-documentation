# Oracle Fusion Fixed Assets setup

## Prorate conventions

**Navigation: Setup > Asset System > Prorate Conventions**

Depreciation start and end are controlled by the prorate convention. Based on the DPIS and the prorate convention the depreciation start date is determined.

With the Depreciate When Placed In Service checkbox checked, depreciation is calculated from the period in which DPIS falls instead of the period in which prorate Date falls as per Prorate Convention setup.
When an asset is retired and has not been fully reserved, then the retirement convention determines the amount depreciated in the last year in service and whether to depreciate in the period of retirement.

The Self-Service Toolkit in Metalink contains a section on the Prorate Convention Setup with documentation, Frequently Asked Questions, and Troubleshooting:

**Top Tech Docs > E-Business Suite: ERP > Assets > Convention**

## Depreciation Books

**Navigation: Setup > Asset System > Book Controls**

There are three types of Depreciation Books: The Corporate Book into which the invoice lines from Oracle Payables or Oracle Projects flow. It is the main depreciation book from which journal entries are created for General Ledger. From the corporate book, the transactions can be copied into the Tax Book. It is called a tax book because it is generally used to keep the tax depreciation. One can maintain different depreciation methods and lives from the corporate book for the same assets. The accumulated depreciation of previous fiscal years can only be adjusted for tax books. After one creates a Budget Book and budget assets, one can run budget reports and project depreciation expenses for amounts budgeted for each category.

When setting up the depreciation books, one defines which set of books and therefore which Accounting Flexfield/Calendar/Currency will be the basis and for which set of books journal entries will be created. The depreciation and prorate calendar need to be chosen. The current open period needs to be chosen and the method for dividing the annual depreciation amount over the periods in the fiscal year.

The accounting rules have to be chosen and the profit/loss accounts that the account generator will use to create the account combinations. The journal categories for the journal entries in General Ledger have to be chosen.

The Self-Service Toolkit in Metalink contains a section on the Depreciation Book Setup with documentation, Frequently Asked Questions, and Troubleshooting:

**Top Tech Docs > E-Business Suite: ERP > Assets > Setup - Book Controls**

## Asset Category

**Navigation: Setup > Asset System > Asset Categories**

The asset categories and depreciation books are now joined and the asset cost/reserve account per book is defined here. Category information is common for a group of assets. Oracle Assets defaults these depreciation rules when you add an asset, to help add assets quickly. If the default does not apply, one can override many of the defaults for an individual asset in the Asset Details or Books windows. Default values are set up for each category in each book. The default depreciation rules that one sets up for a category also depend upon the date placed in the service ranges specified.

The Self-Service Toolkit in Metalink contains a section on the Asset Category Setup with documentation, Frequently Asked Questions, and Troubleshooting:

**Top Tech Docs > E-Business Suite: ERP > Assets > Setup - Categories**

# Account Generator

Before the first asset is added to the system the rules used to create the accounts for the journal entries in General Ledger have to be defined. Oracle Assets works only with transactions. Every transaction with financial impact is translated by the system into a standard journal entry. The Account Generator is needed to fill these fixed journal entries with account combination values.

The Self-Service Toolkit in Metalink contains a section on the Account Generator Setup with documentation, Frequently Asked Questions,s and Troubleshooting:

**Top Tech Docs > E-Business Suite: ERP > Assets > Workflow/Flexbuilder**

**Top Tech Docs > E-Business Suite: ERP > Assets > Generate Accounts**

## Check your setup

Before the first asset is added to the system the system setup should be checked. Oracle Support provides two scripts, which not only check the setup of Oracle Assets and report on it but also show issues and problems and give links to Notes on how to correct these setup issues. It is highly recommended to run these scripts.

## Asset Additions

There are three ways in Oracle Assets to create an asset addition:

* DetailAddition
* QuickAddition
* MassAddition

An asset can only be added to one corporate book. It can however be added to several tax books.

**Navigation: Assets > Asset Workbench > New**

Use this method if Oracle Payables is not installed. To benefit from the integration, if Oracle Payables (AP) is installed, the invoices coming from AP can be prepared for addition in the Prepare Mass Additions form.
