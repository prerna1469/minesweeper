public class Main
{
	public static void main(String[] args) 
	{
	

public class Main {BufferedReader br=new BufferedReader(new InputStreamReader(System.in)); 
int choice,score,flag,r,c;
void accept() { 
do {

System.out.println("enter row index");

r=Integer.parseInt(br.readLine());
System.out.println("enter column index"); 
c=Integer.parseInt(br.readLine());

  }
while (choice!=3);
}
void check1()
{int i,j;
    int[][] a1={
        {1,1,0,1},
        {1,0,1,1},
        {1,1,1,1},
        {1,0,1,0},
    };
    
    if((r==1 && c==3) ||(r==2 && c==2)||(r==4 &&c==2)|| (r==4 && c==4))
    score=0;
    else 
    {score++;
    System.out.println("score=",score);
    }
    
    
     return score;
    
    
}

void display()
{
    do
    {
        flag=0;
        int score1=check1();
        if(score1==12)
        {
            System.out.println("you won");
            flag=1;
            break;
        }
    }
    while(flag==1);
    if(flag==0)
    {
        System.out.println("you lost");
        System.out.println("the array was");
        for(int i=0;i<4;i++)
        {
            for(int j=0;j<4;j++)
            {
                System.out.println(a1[i][j]);
            }
        }
        
        
    }
}

public static void main(String[] args)
{int choice1;
    System.out.println("1. user 1");
    System.out.println("2. user 2");
    System.out.println("3. exit");
    System.out.println("enter choice");
    choice1=Integer.parseInt(br.readLine());
    switch (choice1)
    {
        case 1: Main ob= new Main();
                 ob.accept();
                 ob.check1();
                 ob.display();
                 break;
                 
   case 2: Main ob1= new Main();
                 ob1.accept();
                 ob1.check1();
                 ob1.display();
                 break;
   case 3: System.out.println("game over");
   break;
    }

} }

    
	}
}
