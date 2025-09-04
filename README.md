# Odoo 17 Venezuelan Localization – Code Review Repository

## Purpose
This repository was created to document and track **code review issues** found in several custom Odoo 17 modules developed by **S2CTechSoporte** for Venezuelan localization.  
The main goal is to identify **bad practices, coding errors, and potential fiscal risks or fraud** within these modules.

## Scope of Review
We are focusing on four Python files:

- `account_wh_islr_doc_invoices.py`
- `account_wh_iva.py`
- `account_wizard_libro_resumen.py`
- `municipality_tax.py`

These files are under detailed inspection, and issues will be created for each detected problem.

## Key Findings to Address
During the review, we are particularly looking for (and have already observed) the following issues:

- **Variable naming inconsistencies**:  
  Many variables are written in *Spanglish* (mix of Spanish and English), reducing code readability.

- **Untranslated messages**:  
  Error messages and strings are written in either Spanish or English, without using Odoo’s proper translation mechanisms (`_()`).

- **Commented-out code**:  
  Legacy code remains in place but is disabled with comments, cluttering the source files.

- **Placeholder or incomplete methods**:  
  Some methods contain no logic and simply return `True`, which is misleading and suggests incomplete implementation.

- **TODO markers left in production code**:  
  Several methods and sections include `TODO:` comments, indicating pending changes that have not been implemented.

- **Incorrect currency handling**:  
  Instead of using the standard `currency._convert()` method provided by Odoo, manual and error-prone conversion logic is used.

## Next Steps
- Individual **GitHub issues** will be created for each identified problem, with detailed explanations and code snippets.  
- The **README will be updated** to summarize all documented issues once the review is complete.  
- The ultimate goal is to provide a clear roadmap for refactoring these modules to meet Odoo’s coding standards and avoid fiscal or accounting risks.

---
✍️ *This repository is for code auditing purposes only. It is not intended to run the modules, but to ensure their compliance with best practices and fiscal transparency.*
