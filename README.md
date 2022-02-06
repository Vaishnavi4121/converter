interface conversions
{
  double  gm_to_kg=1000;
  public double gmtokg(double gm);
  public double kgtogm(double kg);
}


class convert implements conversions
{
    public double gmtokg(double gm)
    {
        
     return gm/gm_to_kg;
    
    }
    public double kgtogm(double kg)
    {
        return kg*gm_to_kg;
          
    }
}


class implIface
{
    public static void main(String args[])
    {
        convert  convobj=new convert();
       conversions c;
       c=convobj;
        System.out.println("2000gm="+c.gmtokg(2000)+"Kg");
     System.out.println("5kg="+c.kgtogm(5)+"gm");
     
    }
}
