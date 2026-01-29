# Prevent User Deletion in ServiceNow

## Project Description
This project implements a Business Rule in ServiceNow to prevent deletion of a user if the user is assigned to any incident.

## Objective
To ensure data integrity by blocking deletion of users who are linked to active incidents.

## Implementation
A Business Rule is created on the `sys_user` table with:
- When: Before Delete
- Script checks if the user is assigned to any incident
- If true, deletion is aborted with an error message

## Steps Performed
1. Created two users (Ajay and Akhil)
2. Created an incident
3. Assigned the incident to Ajay
4. Created Business Rule to prevent deletion
5. Tried deleting Ajay (blocked)
6. Deleted Akhil (allowed)

## Output
- Assigned user cannot be deleted
- Unassigned user can be deleted

## Screenshots
Screenshots are added to show:
- User creation
- Incident creation
- Business rule
- Delete blocked
- Delete allowed
