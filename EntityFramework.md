
####Azure Code first approach to create service

1. Create Model file in new MVC app

2. Create MVC and API controller using scafolding providing the model file and new data context.

3. Run the service - it will create tables with name same as model name. 

Add below in YourDbContext.cs

protected override void OnModelCreating(DbModelBuilder modelBuilder)
{
    Database.SetInitializer<YourDbContext>(null);
    base.OnModelCreating(modelBuilder);
}
........................

Update Table or add new Table will give error. So need migration every time you make changes
https://msdn.microsoft.com/en-gb/data/jj554735.aspx

Run below 2 commands in Package Manager Console ->  First command is one time and it will generate Migrations folder 
in your project which will contain Configuration file containing context.
Enable-Migrations –EnableAutomaticMigrations
Update-Database


If Update-Database gives error
use Update-Database -Verbose
and if you are sure that there would be no loss of data, use with force option.
Update-Database -Force
