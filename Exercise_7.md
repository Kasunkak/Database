## Question 1
### Vesa flies from his current location to the Nottingham Airport. At the same time, Vesa's carbon footprint increases by 500. Update the information to the database.
UPDATE game
SET location = (SELECT ident FROM airport WHERE name = "Nottingham Airport"),
co2_consumed = co2_consumed + 500
WHERE screen_name = "Vesa";

![Q1](https://github.com/user-attachments/assets/1a540512-bee4-463c-bccd-dfb2788769b3)

## Question 2
### Prepare your own database for the project by deleting all dummy data relating to the game state. To maintain referential integrity, you have to delete the data in a specific order.

![Q2](https://github.com/user-attachments/assets/773300df-0b2e-4fab-bb34-72aadc79a792)

## Question 3
### Delete the dummy data from the goal_reached table.
DELETE FROM goal_reached;

![Q3](https://github.com/user-attachments/assets/e093cdb3-c3c3-40f6-b669-57282e11f204)

## Question 4
### Delete the data from the game table.
DELETE FROM game;

![Q4](https://github.com/user-attachments/assets/48270410-c4d1-4fd7-b419-3c096f2f4707)
