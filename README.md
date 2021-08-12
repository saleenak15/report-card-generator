# report-card-generator
#include<stdio.h>


int main()  {
  
  char name [50],section [4],grade='X';     // user input student name and section
  int standard,mathematics,english,hindi,science,socialScience;      // user input student's subject marks
  float totalMarks; 
  
  printf (" Please Enter Student Name:");
  scanf ("%[^\n]", name);
  
  printf ("\nPlease Enter standard of Student:");
  scanf ("%d",&standard);
  
  while ((getchar())!='\n');
  
  printf ("\nPlease Enter Section of Student:");
  scanf ("%s", &section);
  
  // Serially type marks for Mathematics, English, Hindi, Science, Social Science

  printf ("\nPlease Enter Mathematics Marks:");
  scanf ("%d", &mathematics); 
  
  printf ("Please Enter English Marks:");
  scanf ("%d",&english);
  
  printf ("Please Enter Hindi Marks:");
  scanf ("%d",&hindi);
  
  printf ("Please Enter Science Marks:");
  scanf ("%d", &science);
  
  printf ("Please Enter Social Science Marks:");
  scanf ("%d", &socialScience);
  
  totalMarks = mathematics+english+hindi+science+socialScience;    //total marks secured by student
  
  
   if (totalMarks>=450 && totalMarks<=500)  {
     grade = 'A'; 
   } else if (totalMarks>=400 && totalMarks<=449)  {
     grade = 'B'; 
   } else if (totalMarks>=350 && totalMarks<=399)  {
     grade = 'C'; 
   } else if (totalMarks>=300 && totalMarks<=349)  {
     grade = 'D'; 
   } else if (totalMarks>=200 && totalMarks<=299)  {
     grade = 'E'; 
   } else if (totalMarks>=0 && totalMarks<=200)  {
     grade = 'F'; 
   } else {
     
     puts ("\n Invalid Input. Please Enter Your Marks between 0 to 500.");
     
   }
   
  puts ("\n\n\t\t\t\t************************");
  puts ("\t\t\t\t--------WELCOME---------");
  puts ("\t\t\t\t************************\n");
  puts ("----------------------------------- ");
  puts ("\t\t Jawahar Navodaya Vidyalaya");
  puts ("\t\t\t\t\t Annual Report Card\n");
   
  printf ("\nName:%s\n",name);  
  printf ("Standard:%d\n", standard);
  printf ("Section:%s\n", section);
  usleep (500000);
  
  printf ("\nMarks Secured out of 100:\n");
  
  printf ("Mathematics:%d\n", mathematics);
  printf ("English:%d\n",english);
  printf ("Hindi:%d\n",hindi);
  printf ("Science:%d\n", science);
  printf ("Social Science:%d\n\n", socialScience);
  usleep (500000);
  
  printf ("Total Marks Secured:%.1f\n\n", totalMarks);
  
    if (grade!= 'X')  
        printf("Grade:%c\n", grade);
        
   puts ("\n\t\t******** THANK YOU ********");    
   puts ("------------------------------------");
   
   return 0;
}
