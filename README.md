
# Secret Santa Employee Game

## How it works

- Admin uses the `/admin` page to manage employees and store up to 5 favorite gift items for each person (data saved in MySQL using a Spring Boot backend).

- The `/game` page loads the same employees and treats them like name slips in a box.

- When a person enters their name on the game page:
  - The app checks that the name exists in the employees list.
  - The app checks that this person has not drawn before (only one chance).
  - The app randomly selects another employee from the list (never the same person).
  - The selected employee is removed from the “box” so nobody else can draw the same name.

- After the draw:
  - The app uses that employee’s stored favorite items to randomly pick one final gift with a spinner.
  - The screen tells the player which gift to buy for that person.
  - In real life, the player keeps the name secret and brings a wrapped gift for the exchange day.
