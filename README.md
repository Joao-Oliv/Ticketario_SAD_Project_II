# TICKETARIO

This has the goal goal to implemente a ticket manage system.

## Project requirements

1. Event Data Storage

Each event must track the following mandatory attributes:

- Name: Title of the event.

- Date: When the event occurs.

- Base Price: The standard unit value for the event.

- Maximum Capacity: The limit of attendees allowed.

- Sold Tickets List: A collection to store all processed tickets.

2. Ticket Data Storage

All tickets must be nominal (assigned to a specific person) and contain:

- Owner Name

- CPF (Individual Registration)

- Associated Event: A reference to the specific event the ticket belongs to.

3. Ticket Categories & Pricing

There are three categories of tickets, each with a specific pricing rule based on the event's base price:

| Category	        | Pricing Logic            |
|-------------------|--------------------------|
| Standard (Pista)	| Base Price (no increase) |
| VIP	            | Base Price + 30%         |
| Cabin (Camarote)	| Base Price + 60%         |

4. Required Methods

For Ticket Classes:

- Calculate Value: A method to compute the final price based on the category percentages mentioned above.

- Show Summary: Displays the owner's name, CPF, and event details (Name and Date).

- Print Value: Returns the ticket type/category along with its specific calculated price.

For the Event Class:

- Sell Ticket: Adds a new ticket to the internal list. Constraint: Must check if the event has reached its maximum capacity before adding.

- Show Sales Count: Returns the total number of tickets currently in the "Sold Tickets" list.