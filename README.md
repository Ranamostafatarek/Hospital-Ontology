# HOSPITAL ONTOLOGY PROJECT

# 1.	Problem Statement:

We are representing a case study of a “Hospital System” by means of Ontologies and Semantic Web.

The hospital system includes Doctors, Nurses, Patients, a Pharmacy, Receptionists, Medicines, and Wards. 

The project will be implemented in “Owl” through Protégé and it will be illustrated in details through an RDF diagram, a detailed RDF 

description, entities cardinality constraints, and finally, we will show several examples for info that are extracted using SPARQL queries. 


# 2.	Detailed RDF Description:

Classes:
Person
Doctor 
Ward 
Nurse 
Pharmacy
Receptionist 
Patient
Medicine

Data Properties:
Person: Full_Name, Phone_Number, Address, ID

Doctor: Speciality

Patient: Ward_Id

Nurse: Shift_Period 

Receptionist: Shift_Period

Ward: ID, Floor

Medecine: Expiry_Date, Name

Pharmacy: Floor, Working_Hours

Object Properties:
Take_Care_of
Register
Treat
Assign
Nurse_at
Supervise
Buy
Prescribe
Hold
Check_in


# 3.	Entities Cardinality Constraints:


•	Doctor
-	prescribe min 1 Medicine
-	supervise min 1 Ward
-	treat max 3 Patient


•	Nurse
-	nurse_at max 2 Ward
-	take_care_of max 4 Patient

•	Patient
-	check_in exactly 1 Ward
-	buy min 1 Medicine

•	Pharmacy
-	hold min 1 Medicine


•	Receptionist
-	assign min 1 Doctor
-	assign min 1 Nurse
-	register min 1 Patient 


•	Ward
-	check_in max 6 Patient
-	nurse_at min 2 Nurse
-	supervise exactly 1 Doctor





# 4.	SPARQL Queries Presented Above:

•	Query to extract Patients and their Doctor’s names.

•	Query to extract Patients, their Doctors and their Specialty

•	Query to extract Patients, their Address and Phone Number.

•	Query to extract Patients, their Nurses and their Shifts.

•	Query to extract Receptionists, their registered Patients and their Wards.

•	Query to extract Receptionists, their Shifts and Phone Number.

•	Query to extract Patients’ Names.

•	Query to extract Doctors’ Names.

•	Query to extract Receptionist’ Names.

•	Query to extract Nurses’ Names.
