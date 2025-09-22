# sql-task-1-
CREATE database libarary;
CREATE TABLE libarary.Members (
    MemberID INT AUTO_INCREMENT PRIMARY KEY,
    Name VARCHAR(100) NOT NULL
);
CREATE TABLE libarary.Book(
    BookID INT AUTO_INCREMENT PRIMARY KEY,
    Title VARCHAR(100) NOT NULL
);
CREATE TABLE libarary.Loans (
    LoanID INT AUTO_INCREMENT PRIMARY KEY,
    MemberID INT,
    BookID INT,
    LoanDate DATE,
    FOREIGN KEY (MemberID) REFERENCES Members(MemberID),
    FOREIGN KEY (BookID) REFERENCES Books(BookID)
);
