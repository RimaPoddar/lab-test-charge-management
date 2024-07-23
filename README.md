# lab-test-charge-management


This project contains a Python implementation for calculating the total charges for lab tests performed by patients in a hospital.

## Overview

The system includes:
- `LabTestRepository` class: Manages lab test IDs and their corresponding charges.
- `Patient` class: Stores patient details and calculates total lab test charges based on the tests performed.

## Classes

### LabTestRepository

- **Static Lists**:
  - `__list_of_hospital_lab_test_ids`: List of available lab test IDs.
  - `__list_of_lab_test_charge`: List of charges corresponding to each lab test ID.
  
- **Methods**:
  - `get_test_charge(lab_test_id)`: Returns the charge for a given lab test ID. Returns -1 if the ID is invalid.

### Patient

- **Instance Variables**:
  - `__patient_id`: ID of the patient.
  - `__patient_name`: Name of the patient.
  - `__list_of_lab_test_ids`: List of lab test IDs performed by the patient.
  - `__lab_test_charge`: Total charge for the lab tests performed by the patient.

- **Methods**:
  - `calculate_lab_test_charge()`: Calculates the total charge for the tests performed by the patient and updates `__lab_test_charge`.


## Example

```python
lab_test_list1 = ["L101", "L103", "L104", 'L105']
patient1 = Patient(1010, "Sam", lab_test_list1)
patient1.calculate_lab_test_charge()
print("Patient id:", patient1.get_patient_id())
print("Patient name:", patient1.get_patient_name())
print("Patient's test ids:", patient1.get_list_of_lab_test_ids())
print("Total lab test charge:", patient1.get_lab_test_charge())
