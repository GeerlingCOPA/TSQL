# T-SQL Conventions

This document summarizes the agreed T-SQL conventions:

1. **Semicolon and Separation:** No unnecessary semicolons should be used. Use `GO` for separation between program parts.
2. **Naming Convention:** Program parts typically start with the prefix `COP_`.
3. **Documentation:** Use `MS_Description` for documentation purposes. Utilize `dbo.cop_sp_modifyextendedproperty` to implement this.

## Example Usage

```sql
-- Example of a GO-separated batch
SELECT * FROM Customers;
GO
SELECT * FROM Orders;
GO

-- Example of a procedure with COP_ prefix
CREATE PROCEDURE COP_GetCustomerDetails AS
BEGIN
    -- Procedure logic
END;

-- Example of documenting an object
EXEC dbo.cop_sp_modifyextendedproperty
    @name = 'MS_Description',
    @value = 'This procedure retrieves customer details',
    @level0type = 'SCHEMA',
    @level0name = 'dbo',
    @level1type = 'PROCEDURE',
    @level1name = 'COP_GetCustomerDetails';
```