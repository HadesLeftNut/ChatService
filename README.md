# ChatService
C# WCF Chat Service, Polling, WPF

2 codes:
1 Service code
1 Client code in WPF

1 Computer runs Service
2 Computers run Client

Connection over phone Hotspot with Discovery Service

Client code:
has 3 TextBoxes (OutputBox for *currently* status updates and display of messages / InputBox for sending messages / UserList for later to display names of users connected to the service)
has 4 Buttons (Send / Receive / What service am I / Test)
has 5 Operation Contracts
works as intended (99% sure)

Service code:
handles the same 5 Operation Contracts
Issues:
Service only accepts connection from Client if the client and the service are running from the same computer.
Example: Laptop 1 runs Service
         Laptop 1 runs Client
         It connects and it works
         OR
         Latop 1 runs Service
         Laptop 2 runs Client
         Client does not connect. Error thrown from RegisterClient Method
Additionally had some issues with the ReceiveMessages Method
