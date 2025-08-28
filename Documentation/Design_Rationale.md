## 1. Database Structure
The system will use a **relational database** because it provides strong data integrity and makes it easier to manage links between entities.
The entities are:
**Lecture** - Stores lecture details such as LectureID, Name, and department.
**Claim** - records claim details such as ClaimID, LecturerID, HoursWorked, HourlyRate, TotalAmount, and Status
**SupportingDocument** - Keeps information about uploaded file, including DocumentID, ClaimID, FilePath, and uploadDate.
**Approval** - Tracks the verification process with ApprovalID, ClaimID, ApprovalDate, and Role (Coordinator or Manager)

**Relationship**
- One lecture can submit many class.
- Each claim can have multiple supporting documents.
- Each claim must go through one or more approval
....

## 2 GUI layout
the system uses ASP.NET Core MVC for the graphical user interface (GUI). The design is role-based :
**Lecture**
- Submit a new claim
- Upload supporting documents.
- Track the Claim status.

**Programme Coordinator**
- Review submitted claims.
- Approve or reject claims 
.

**Academic Manager**
- Review submitted claims
- View claim history and reports

## 3 Assumptions
- lectures will register and log in before submitting claims
- Coordinators and Managers will access a separate admin portal with own logins
- Claims must always include hours, rates, and supporting documents.
- All communication between roles happens within the system (no uutside emailing needed).

## 4 Contraints


## 5 Purpose of this document
- This file serves as a **working draft** of the design rationale.
- It is mainly for Github Tracking, showing my design thought process.
