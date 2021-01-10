#include iostream
  
#include cstring
  
using namespace std;

class student

{

    protected:
    
        char *subject;
        
        int marks;
        
        int len;
        
    public:
    
        student()
        
        {
        
            marks=0;
            
            subject=new char[len+1];
            
        }
        
        void getsubject(void)
        
        {
        
            char *s;
            
            s=new char[30];
            
            cout<<"enter subject name";
            
            cin>>s;
            
            len=strlen(s);
            
            subject=new char[len+1];
            
            strcpy(subject,s);
            
        }
        
        void printsubject(void)
        
        {
        
            cout<<subject<<"\n";
            
        }
        
};



int main()

{

    student *cptr[10];
    
    int n=1;
    
    int option;
    
    do{
    
        cptr[n]=new student;
        
        cptr[n]->getsubject();
        
        n++;
        
        cout<<"Doyou wnat to enter 1 more subject? \t\n";
        
        cout<<"enter 1 for yes and 0 for no: \t";
        
        cin>>option;
        
    }
    
    while(option);
    
    
    cout<<"\n\n";
    
    for(int i=1;i<=n;i++)
    
    {
    
        cptr[i]->printsubject();
        
    }
    

    return 0;
    
}
