# README

## Refactor and Normalize Data Structures

As a next step, please refactor and normalize the data models in this application:

- **Normalize Data Structures:**
  - Abstract new classes from the existing models to better represent the domain.

- **OEM Abstraction:**
  - Move the `oem` field out of the `Dealership` model and create a separate `Oem` (Original Equipment Manufacturer) class/model.
  - A `Dealership` should belong to an `Oem`.

- **Car Structure Refactor:**
  - Decompose the `Car` model into the following normalized classes:
    - `Year`
    - `Make`
    - `Model`
    - `Trim`
  - These classes should be related as follows:
    - A `Dealership` has one-to-many `Makes`.
    - A `Make` has one-to-many `Models`.
    - A `Model` has one-to-many `Years` (model years).
    - A `ModelYear` (or similar) has one-to-many `Trims`.
    - A `Car` record should be a composite of these classes (referencing the appropriate year, make, model, and trim).

- **Example Relationships:**
  - `Dealership` → `Make` → `Model` → `Year` → `Trim` → `Car`

This normalization will improve data integrity, reduce redundancy, and make the system more extensible.

---
