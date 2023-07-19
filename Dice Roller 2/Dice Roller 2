Console.WriteLine("Welcome to the Dice Roller! Good luck ;)");

bool runProgram = true;
while (runProgram)
{
    Console.WriteLine("Enter 6 for craps, 10 for Zaxxon or another number for fun:");

    int sides1 = 0;
    while (true)
    {
        try
        {
            sides1 = int.Parse(Console.ReadLine());
            if (sides1 > 0)
            {
                break;
            }
            else
            {
                Console.WriteLine("Please enter a positive number");
            }
        }
        catch
        {

            Console.WriteLine("Enter only numbers please, try again");
        }
    }
 
    int sides2 = sides1;

    if (sides2 == 6)
    {
        Random roll = new Random();

        int score1 = roll.Next(1, sides1 + 1);
        int score2 = roll.Next(1, sides2 + 1);
        int sum = score1 + score2;
        Console.WriteLine($"Die 1 rolled a {score1}");
        Console.WriteLine($"Die 2 rolled a {score2}");
        Console.WriteLine($"You scored a {sum}");
        Console.WriteLine(RollSpecial(score1, score2));
        Console.WriteLine(RollMoney(sum));
    }

    else if (sides2 == 10)
    {
        Random roll = new Random();

        int score3 = roll.Next(1, sides1 + 1);
        int score4 = roll.Next(1, sides2 + 1);
        int minus = score3 - score4;
        Console.WriteLine($"Die 1 rolled a {score3}");
        Console.WriteLine($"Die 2 rolled a {score4}");
        Console.WriteLine($"You scored a {minus}");
        Console.WriteLine(RollZaxx(score3, score4));
        Console.WriteLine(RollZaxx2(minus));
    }

    else
    {
        Random roll = new Random();

        int score1 = roll.Next(1, sides1 + 1);
        int score2 = roll.Next(1, sides2 + 1);
        int sum = score1 + score2;
        Console.WriteLine($"Die 1 rolled a {score1}");
        Console.WriteLine($"Die 2 rolled a {score2}");
        Console.WriteLine($"You scored a {sum}");
    }
    Console.WriteLine("Would you like to continue? y/n");
    string choice = Console.ReadLine();
    if (choice == "n")
    { runProgram = false; }
}

//methods

static string RollSpecial(int score1, int score2)
{
    if (score1 == 1 && score2 == 1)
    {
        return "Snake Eyes!";
    }
    if ((score1 == 1 && score2 == 1) || (score2 == 2 && score1 == 1))
    {
        return "Ace Deuce!";
    }
    if (score1 == 6 && score2 == 6)
    {
        return "Box Cars!";
    }
    else
    {
        return "";
    }
}

static string RollMoney(int sum)
{
    if (sum == 7 || sum == 11)
    {
        return "You win!";
    }
    if (sum == 2 || sum == 3 || sum == 12)
    {
        return "You lose, don't gamble kids";
    }
    else
    {
        return "";
    }
}

static string RollZaxx(int score1, int score2)
{
    if (score1 == 2 && score2 == 2)
    {
        return "2 is the best number!";
    }
    if ((score1 == 2 && score2 == 3) || (score2 == 3 && score1 == 2))
    {
        return "Birds and bees, 2s and 3s";
    }
    if (score1 == 5 && score2 == 5)
    {
        return "$5 footlong";
    }
    else
    {
        return "";
    }
}

static string RollZaxx2(int minus)
{
    if (minus<= - 6 || minus >= 6)
    {
        return "Rode the outside, You win!";
    }
    if (minus >= -2 && minus <= 2)
    {
        return "Too close to the middle, you lose";
    }
    else
    {
        return "Nothing special happened, you should probably retry";
    }
}


