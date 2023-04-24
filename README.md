# DB-backend-2
## Instructions
- Vytvořte webovou aplikaci spravující záznamy v databázi.
- Téma databáze si zvolte sami.
- Stačí jeden entitní typ o minimálně 4 atributech a minimálně 3 datových typech.
- Aplikace bude umět vkládat(formulář), upravovat(formulář), mazat(optání) a zobrazovat(tabulka) jednotlivé záznamy.
- Pro frontend použijte HTML, CSS (SASS, SCSS) a JS.
- Pro backend použijte jazyk dle vašeho uvážení z nabízených: PHP, JS(node.js), Python, Java
- DBMS může být jedna z uvedených: MySQL, MariaDB, PostgreSQL, MongoDB.
- Aplikace nemusí být OOP ani MVC, OOP a MVC jsou však body navíc.
- Nemusí být responzivní ani přístupná, ale opět jsou to body navíc.
- Nemusíte řešit přihlašováním práva atp.
- Napište základní README.md se seznámením s aplikací a několika ukázkami (zmenšené screenshoty). 
- Odevzdávejte jako odkaz na repo projektu na githubu.


##  Screenshots
### Clients
![clients](https://user-images.githubusercontent.com/92713632/233860213-5c68c4af-44ac-4ff9-bb58-ad1e226fcd68.jpg)
### New Client / requirement 
![field_required](https://user-images.githubusercontent.com/92713632/233860296-b627502c-d909-4b1d-8de9-80db9d329b8d.jpg)
### New Client added
![new_client](https://user-images.githubusercontent.com/92713632/233860217-6d61a649-c5e3-40fd-947a-8d796c383e06.jpg)


### SQL Queries
CREATE TABLE clients (
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR (100) NOT NULL,
    email VARCHAR (200) NOT NULL UNIQUE,
    phone VARCHAR(20) NULL,
    address VARCHAR(200) NULL,
    created_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP
);


INSERT INTO clients (name, email, phone, address)
VALUES
('John Doe', 'john.doe@microsoft.com', '+127256719', 'Nevada, USA'),
('Chris Tucker', 'chris.tucker@gmail.com', '+222223731', 'Ohio, USA'),
('Walter White', 'walter.white@gmail.com', '+8002255324', 'New Mexico, USA'),
('Bob Joey', 'bobby@gmail.com', '+111555999', 'Hawaii, USA'),
('Rick Roll', 'rick.roll@gmail.com', '+324426235', 'Manchester, England'),
('John Lennon', 'john.lennon@gmail.com', '+2569235655', 'Bristol, England');
