```mermaid
erDiagram
    Customer ||--o{ Product : Buys 
    Customer }|..|{ Sale : Makes
    Customer {
        string firstName
        string lastName
        int age
    }
    Product ||--o{ Inventory : "Is In"
    Product {
        string costtobuyShoe
        string totalshoeSold
        string costtoproduceShoe PK
    }
    Inventory ||--o{ Product : Holds
    Inventory{
        string amountofShoe PK, FK
        string totalcostofInventory  FK
    }
    Sale ||--o{ Inventory : "Takes From"
    Sale{
        string moneyMade
        string totalshoeSold FK
    }



