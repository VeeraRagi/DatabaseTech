A SQL Database server is a 
	logical construct 
	that acts as a central administrative point for multiple single or pooled databases, 
		logins, 
		firewall rules, 
		auditing rules, 
		threat detection policies, 
		and failover groups 
A SQL Database server can be in a different region than its resource group.
All databases managed by a SQL Database server are created within the same region as the SQL Database server.

A SQL Database server:
	Is created within an Azure subscription, but can be moved with its contained resources to another subscription
	Is the parent resource for databases, elastic pools, and data warehouses
	Provides a namespace for databases, elastic pools, and data warehouses
	Is a logical container with strong lifetime semantics - delete a server and it deletes the contained databases, elastic pools, and data warehouses
	Participates in Azure role-based access control (RBAC) - databases, elastic pools, and data warehouses within a server inherit access rights from the server
	Is a high-order element of the identity of databases, elastic pools, and data warehouses for Azure resource management purposes (see the URL scheme for databases and pools)
	Collocates resources in a region
	Provides a connection endpoint for database access (<serverName>.database.windows.net)
	Provides access to metadata regarding contained resources via DMVs by connecting to a master database
	Provides the scope for management policies that apply to its databases - logins, firewall, audit, threat detection, and such
	Is restricted by a quota within the parent subscription (six servers per subscription by default - see Subscription limits here)
	Provides the scope for database quota and DTU or vCore quota for the resources it contains (such as 45,000 DTU)
	Is the versioning scope for capabilities enabled on contained resources
	Server-level principal logins can manage all databases on a server
	Can contain logins similar to those in instances of SQL Server on your premises that are granted access to one or more databases on the server, 
	and can be granted limited administrative rights. For more information, see Logins.
	The default collation for all databases created on a SQL Database server is SQL_LATIN1_GENERAL_CP1_CI_AS, 
	where LATIN1_GENERAL is English (United States), CP1 is code page 1252, CI is case-insensitive, and AS is accent-sensitive.
	
		
You can create the Azure SQL database's resource group ahead of time or while creating the server itself. 
There are multiple methods for getting to a new SQL server form, either by creating a new SQL server or as part of creating a new database.	
