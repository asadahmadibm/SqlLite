# SqlLite

Microsoft.EntityFrameworkCore.Design

Microsoft.EntityFrameworkCore.Sqlite

Microsoft.EntityFrameworkCore.Tools for command line

     public class StoreDbContext :DbContext
        {
            public DbSet<Domain.entity.Member> Memberss { get; set; }
            public StoreDbContext(DbContextOptions<StoreDbContext> options) : base(options)
            {
            }
    
        }
	
"ConnectionStrings": {
    "DefaultConnection": "DataSource=Database\\app.db"
},

builder.Services.AddDbContext<StoreDbContext>(options =>
        options.UseSqlite(builder.Configuration.GetConnectionString("DefaultConnection")));

add-migration initial

update-database
