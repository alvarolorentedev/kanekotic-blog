    # The First Day


## Gitbook

So i have started writing using GitBook, to take notes of what i learn every day. a few things have shown up.

1. There are some required files if you start from a GitHub repository that you will have to create:
    * README.md
    * SUMMARY.md


2. Markdown is partially working as per escape characters don't work with &#35; and numbering and listing get confused easyli.

## C&#35;

When doing complex objects using an object to help the building is welcome. 

```csharp
class Complex
{
    double x;
    double y;
    double z;
    
    float height;
    float width;
    
    string foreground;
    string background;
    
    public Complex()
    {
        x = 1.456;
        y = 1.234;
        z = 1.789;
        
        height = 10.12;
        width = 10.14;
    
        foreground = "#FFF";
        background = "#FA1";
    }
    
}
```
In this way you remove some complexity of just adding steps in your constructor to something more abstract and can contain the logic.

```csharp
class Complex
    {
        double X { get; set; }
        double Y { get; set; }
        double Z { get; set; }

        double Height { get; set; }
        double Width { get; set; }

        string Foreground { get; set; }
        string Background { get; set; }

        public void Complex(ComplexBuildHelper buildHelper)
        {
            buildHelper.Construct(this);
        }

    }
    
class ComplexBuildHelper
{
    void BuildPosition(Complex reference)
    {
        reference.X = 1.456;
        reference.Y = 1.234;
        reference.Z = 1.789;

    }

    void BuildDimension(Complex reference)
    {
        reference.Height = 10.12;
        reference.Width = 10.14;
    }

    void BuildCharacteristics(Complex reference)
    {
        reference.Foreground = "#FFF";
        reference.Background = "#FA1";
    }

    public void Construct(Complex reference)
    {
        BuildPosition(reference);
        BuildDimension(reference);
        BuildCharacteristics(reference);
    }
}
```