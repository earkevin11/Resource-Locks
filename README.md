# Resource-Locks

# What are Azure Resource Locks?
- Locking resources can help ensure users do not accidentally delete or modify resources
- There are 2 types of resource locks: CanNotDelete Lock and ReadOnly lock
- Admins can apply locks at the resource level or the resource group level or the subscription level


# Difference between Delete Lock and Read Lock
- Delete Lock - one can read and modify the resource but cannot delete
- Read Lock - one can only read. No modify or delete.

# Remember that locks applied at the Resource Group level will be inherited by the resources
