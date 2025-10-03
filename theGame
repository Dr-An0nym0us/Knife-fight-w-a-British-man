using System; //and so hell begins

class GameStart
{

    public static int playerHealth = 100;
    public static int britHealth = 100;
    public static bool endingTrue = false;

    static void Main(string[] args)
    {

        Console.WriteLine("Hello there, What's your name?");
        string playerName = Console.ReadLine();  //gets player name
        Console.WriteLine("Intersting... " + playerName + ", huh? Nice to meet you, I'm a narrator");
        
        bool booDec = false;

        while (booDec == false)
        {
            Console.WriteLine("So, you have a couple options from here. You could 1. Exit the game. 2. Rename yourself. or 3. Play. \nIt's your call");
            string decision = Console.ReadLine();

            if (decision == "1")
            {  //checks if player says 'leave', so, it ends the program
                Console.WriteLine("bye bye~~");
                Environment.Exit(0);

            }
            else if (decision == "2")
            {  //the player wants to edit their name, so let them
                Console.WriteLine("Alrighty, what do you want me to call you then?");
                playerName = Console.ReadLine();
                Console.WriteLine(playerName + ", huh? interesting...");
                booDec = false;

            }
            else if (decision == "3") //lets the player play the game
            {
                Console.WriteLine("alrighty then, lets play a little game, shall we?");
                booDec = true;
            }

        }

        Console.WriteLine("You awaken in an unfamiliar city, blinding lights fill your vision and thousands of sounds pervade your ears.");
        Console.WriteLine("As you explore around, you notice a man in full black clothing tailing you around every corner you turn.");
        Console.WriteLine("The mysterious man approaches you, his hand gripping something in his pocket.");
        Console.WriteLine("\"Give me your wallet!\" He loudly exclaims, a knife pointed in you direction from his hand.");

        while (endingTrue == false) //et voila, my main turn system
        {
            GameStart.PlayerTurn();
            GameStart.BritTurn();
            if (playerHealth == 0) //checks if player dies
            {
                GameStart.EndingDos();
            }

            if (britHealth == 0) //checks if brit dies
            {
                GameStart.EndingUno();
            }
        }

    }

    public static void BritTurn() //function that makes a random int and depending on its result, it deals according damage to player
    {
        Random chanceHit = new Random();
        int actualHit = chanceHit.Next(1, 101);
        if (actualHit <= 20)
        {
            Console.WriteLine("The man stabs you with his knife. -20 health");
            playerHealth -= 20;
            Console.WriteLine("You are currently at " + playerHealth + " hp");
        }
        else if (actualHit <= 70)
        {
            Console.WriteLine("The man slices you with his knife. -10 health");
            playerHealth -= 10;
            Console.WriteLine("You are currently at " + playerHealth + " hp");
        }
        else if (actualHit <= 100)
        {
            Console.WriteLine("The man grazes you with his knife. -5 health");
            playerHealth -= 5;
            Console.WriteLine("You are currently at " + playerHealth + " hp");
        }
        Console.WriteLine(""); //for text seperation
    }

    public static void PlayerTurn() //player decisions and stuff for their turn
    {
        Console.WriteLine("It's your turn, what do you do?");
        Console.WriteLine("\n1. Fight back. \n2. Run away.");
        string turnDec = Console.ReadLine();
        string turnDecUsed = turnDec.ToLower();
        Console.WriteLine(""); //for text seperation
        switch (turnDecUsed)
        {
            case "1" :
                GameStart.BritDamaged();
                break;
            case "2":
                GameStart.FleeOption();
                break;

        }
    }

    public static void BritDamaged() //USE THIS FOR DAMAGING THE BRIT
    {
        Random random1 = new Random();
        int hitDmg = random1.Next(1, 21);
        if (hitDmg <= 20 && hitDmg >= 15)
        {
            Console.WriteLine("You got a critical hit! he lost 20 hp.");
            britHealth -= 20;
        }
        else if (hitDmg <15 && hitDmg >=5) 
        {
            Console.WriteLine("You got a pretty good hit on him. he lost 10 hp");
            britHealth -= 10;
        }
        else
        {
            Console.WriteLine("You hit the stranger. he lost 5 hp.");
            britHealth -= 5;
        }
        Console.WriteLine("He's now at " + britHealth + " hp");
        Console.WriteLine(""); //for text seperation
    }

    public static void FleeOption() //makes a value for fleeChance, and if its equal to or below 30, it succeeds and gives the player ending 3
    {
        Random random1 = new Random();
        int fleeChance = random1.Next(1, 101);
        if (fleeChance <= 30)
        {
            GameStart.EndingTres();
        }
        else
        {
            Console.WriteLine("Oof, you attempted escape from the battle, but tripped and failed.");
            Console.WriteLine(""); //for text seperation
        }
    }

    public static void EndingTres() //this is just ending three where you escape
    {
        Console.WriteLine("You managed to flee the scene, barely escaping the grasp of the british man as he tries to grab you.");
        Console.WriteLine("As you drift into the city, a faint fog fades in around you.");
        Console.WriteLine("The fog thickens, enveloping your body like a blanket.");
        Console.WriteLine("Your consciousness fades as you wonder, \"Why am i here\" \"Who was that voice?\" \"I could really go for a cheeseburger right now\"");
        Environment.Exit(0);

    }

    public static void EndingDos() //this is ending 2 where you die
    {
        Console.WriteLine("Your breathing grows heavier while you clothes are stained with blood.");
        Console.WriteLine("As your vision fades, the stranger approaches you, quickly grabbing something off of you.");
        Console.WriteLine("Your eyes grow heavy, and the strange man walks away while you collapse on the ground.");
        Console.WriteLine("You died");
        Environment.Exit(0);
    }

    public static void EndingUno() //this is ending 1 where the brit dies
    {
        Console.WriteLine("The mysterious man starts bleeding profusely from the stab wounds.");
        Console.WriteLine("He starts to run away, before collapsing on the ground.");
        Environment.Exit(0);
    }

}



