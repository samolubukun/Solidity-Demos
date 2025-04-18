# Solidity-Demos
Introductory Solidity smart contracts showcasing fundamental concepts through practical examples: a lottery, a crowdfunding campaign, and an event management system.

## Simple Lottery System

This Solidity smart contract implements a simple lottery system. The contract has a designated `manager` who is responsible for initiating the lottery and picking the winner. Participants can enter the lottery by paying a fixed amount of 1 ether. Once at least three players have joined, the manager can trigger the `pickWinner` function. This function uses a pseudo-random number generator to select a winner from the pool of participants, transfers the entire lottery balance to the winner, and then resets the player list for a new round. Only the manager has the authority to check the contract's balance and pick the winner.

## Decentralized Crowdfunding Campaign

This Solidity smart contract facilitates a crowdfunding campaign managed by a designated `manager`. Users can contribute funds (minimum contribution enforced) before a set `deadline`. If the `target` amount is not reached by the deadline, contributors can request a refund. The manager can create spending `requests` for the raised funds, which contributors can then vote on. Payments for these requests are executed by the manager only if the campaign target is met and a majority of contributors have voted in favor of the request.

## Decentralized Event Organization and Ticketing

This Solidity smart contract enables decentralized event organization and ticketing. Organizers can create events by specifying the name, date (as a Unix timestamp), ticket price, and the total number of tickets available. Attendees can purchase tickets for a specific event by sending the exact required Ether. The contract keeps track of remaining tickets and the number of tickets each address holds for each event. Ticket holders can also transfer their tickets to other addresses before the event occurs.
