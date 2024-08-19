# Hotelaria System
## Overview
Projeto basico de hospedagem para o desafio de projetos da DIO curso de .NET

## Features
* Register guests for a reservation.
* Assign a suite to a reservation.
* Calculate the total cost of a stay based on the number of days reserved.
* Apply a discount for long stays (10 days or more).
## Getting Started
Prerequisites
* .NET SDK (version 5.0 or later)
## Installation
1. Clone the repository:

```bash
git clone https://github.com/your-username/hotelaria-system.git
```
2. Navigate to the project directory:

```bash
cd hotelaria-system
```
3. Restore dependencies:
```bash
dotnet restore
```
4. Build the project:

```bash
dotnet build
```
## Running the Application
To run the application locally, use the following command:

```bash
dotnet run
```
## Usage
Example 1: Registering Guests
```csharp
Copiar código
// Create a new reservation
var reserva = new Reserva(5);

// Register guests
var hospedes = new List<Pessoa>
{
    new Pessoa { Nome = "John Doe" },
    new Pessoa { Nome = "Jane Doe" }
};
reserva.CadastrarHospedes(hospedes);
```
Example 2: Assigning a Suite
```csharp
Copiar código
// Create a new suite
var suite = new Suite
{
    Capacidade = 2,
    ValorDiaria = 100m
};

// Assign the suite to the reservation
reserva.CadastrarSuite(suite);
```
Example 3: Calculating the Total Cost
```csharp
Copiar código
// Calculate the total cost of the stay
decimal totalCost = reserva.CalcularValorDiaria();
Console.WriteLine($"Total cost: {totalCost:C}");
```