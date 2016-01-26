    # The First Day


## Gitbook

So i have started writing using GitBook, to take notes of what i learn every day. a few things have shown up.

1. There are some required files if you start from a GitHub repository that you will have to create:
    * README.md
    * SUMMARY.md


2. Markdown is partially working as per escape characters don't work with &#35; and numbering and listing get confused easyli.

## C&#35;

When doing complex objects a builder pattern is always welcome, I found myself refactoring code due this Today. 

```csharp
public class Complex
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
    public interface IBuildHelper<T>
    {
        void Construct(T reference);
    }

    public class Complex
    {
        class ComplexBuildHelper : IBuildHelper<Complex>
        {
            void BuildPosition(Complex reference)
            {
                reference.x = 1.456;
                reference.y = 1.234;
                reference.z = 1.789;

            }

            void BuildDimension(Complex reference)
            {
                reference.height = 10.12;
                reference.width = 10.14;
            }

            void BuildCharacteristics(Complex reference)
            {
                reference.foreground = "#FFF";
                reference.background = "#FA1";
            }

            public void Construct(Complex reference)
            {
                BuildPosition(reference);
                BuildDimension(reference);
                BuildCharacteristics(reference);
            }
        }

        double x;
        double y;
        double z;

        double height;
        double width;

        string foreground;
        string background;

        Complex()
        {
            var buildHelper = new ComplexBuildHelper();
            buildHelper.Construct(this);
        }

    }
    
    ```