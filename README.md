# Resource-Locks

# What are Azure Resource Locks?
- Locking resources can help ensure users do not accidentally delete or modify resources
- There are 2 types of resource locks: CanNotDelete Lock and ReadOnly lock
- Admins can apply locks at the resource level or the resource group level or the subscription level


# Difference between Delete Lock and Read Lock
- Delete Lock - one can read and modify the resource but cannot delete
- Read Lock - one can only read. No modify or delete.

# Important reminders:
- Remember that locks applied at the Resource Group level will be inherited by the resources
- Locks applied at the subscription level will also be inherited down.

# Use Cases:
- Admins can apply resource locks to across multiple subscriptions and lock their resources via Blueprints


# Before, we assigned a Blueprint to create a resource group without a lock
- This would mean that we can delete the resource group wiithout error


# Say we unassign the Blueprint and then reassign the Blueprint with a DoNotDelete lock
- Now, subscription owners would not be able to delete.
- The lock wouldn't be visible under locks. 
- Blueprints uses the "Deny Assignments" to lock your resources.
- To delete the resource group, one must unassign the Blueprint.

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/175822371-82070a59-9c1e-4297-8121-5c91a1b878f4.png" height="65%" width="65%" alt="Resource Locks"/>

<p/>

