---
layout: post
title: Form Binding in Blazor DataForm Component | Syncfusion
description: Checkout and learn here about Model ,EditContext and Custom Validation attributes binding with Blazor DataForm component.
platform: Blazor
control: DataForm
documentation: ug
---

# Data annotation attributes

The DataForm component enables users to define the data annotation attributes available from the instance of [System.ComponentModel.DataAnnotations](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.dataannotations?view=net-5.0). 

## Display attribute

The [DisplayAttribute](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.dataannotations.displayattribute?view=net-5.0) class is used to specify the display name for a property. The display name is used as the label for the corresponding editor in the DataForm component if label text is not specified for the form item. 

{% tabs %}
{% highlight C# tabtitle="C#"  %}

[Display(Name = "Name")]
public string Name { get; set; }

{% endhighlight %}
{% endtabs %}

## Validation attributes

The DataForm component supports the following validation attributes from the [System.ComponentModel.DataAnnotations](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.dataannotations?view=net-5.0) namespace.

### Required attribute

The [RequiredAttribute](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.dataannotations.requiredattribute?view=net-5.0) class is used to specify that a property is required. The DataForm component displays an error message if the property is empty. 

{% tabs %}
{% highlight C# tabtitle="C#"  %}

[Required(ErrorMessage = "Name is required")]
public string Name { get; set; }

{% endhighlight %}
{% endtabs %}

### Range attribute

The [RangeAttribute](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.dataannotations.rangeattribute?view=net-5.0) class is used to specify the numeric range constraints for the value of a property. The DataForm component displays an error message if the property value is not within the specified range. 

{% tabs %}
{% highlight C# tabtitle="C#"  %}

[Range(0, 100, ErrorMessage = "Age must be between 0 and 100")]
public int Age { get; set; }

{% endhighlight %}
{% endtabs %}

### Regular expression attribute

The [RegularExpressionAttribute](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.dataannotations.regularexpressionattribute?view=net-5.0) class is used to specify that a property value must match a specified regular expression. The DataForm component displays an error message if the property value does not match the specified regular expression. 

{% tabs %}
{% highlight C# tabtitle="C#"  %}

[RegularExpression(@"^[a-zA-Z]+$", ErrorMessage = "Name must contain only alphabets")]
public string Name { get; set; }

{% endhighlight %}
{% endtabs %}

### String length Attribute

The [StringLengthAttribute](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.dataannotations.stringlengthattribute?view=net-5.0) class is used to specify the minimum and maximum length constraints for the value of a property. The DataForm component displays an error message if the property value is not within the specified length constraints. 

{% tabs %}
{% highlight C# tabtitle="C#"  %}

 [StringLength(100, MinimumLength = 3, ErrorMessage = "Name must be between 5 and 10 characters")]
 public string Name { get; set; }

{% endhighlight %}
{% endtabs %}

### Minimum length Attribute

The [MinLengthAttribute](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.dataannotations.minlengthattribute?view=net-5.0) class is used to specify the minimum length constraints for the value of a property. The DataForm component displays an error message if the property value is not within the specified length constraints. 

{% tabs %}
{% highlight C# tabtitle="C#"  %}

[MinLength(3, ErrorMessage = "Name must be at least 3 characters")]
public string Name { get; set; }

{% endhighlight %}
{% endtabs %}

### Maximum length Attribute

The [MaxLengthAttribute](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.dataannotations.maxlengthattribute?view=net-5.0) class is used to specify the maximum length constraints for the value of a property. The DataForm component displays an error message if the property value is not within the specified length constraints. 

{% tabs %}
{% highlight C# tabtitle="C#"  %}

[MaxLength(10, ErrorMessage = "Name must be at most 10 characters")]
public string Name { get; set; }

{% endhighlight %}
{% endtabs %}

### Phone number attribute

The [PhoneAttribute](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.dataannotations.phoneattribute?view=net-5.0) class is used to specify that a property value must match a specified phone number pattern. The DataForm component displays an error message if the property value does not match the specified phone number pattern. 

{% tabs %}
{% highlight C# tabtitle="C#"  %}

[Phone(ErrorMessage = "Phone number is not valid")]
public string PhoneNumber { get; set; }

{% endhighlight %}
{% endtabs %}

### Email address attribute

The [EmailAddressAttribute](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.dataannotations.emailaddressattribute?view=net-5.0) class is used to specify that a property value must match a specified email address pattern. The DataForm component displays an error message if the property value does not match the specified email address pattern. 

{% tabs %}
{% highlight C# tabtitle="C#"  %}

[EmailAddress(ErrorMessage = "Email address is not valid")]
public string Email { get; set; }

{% endhighlight %}
{% endtabs %}

### URL attribute

The [UrlAttribute](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.dataannotations.urlattribute?view=net-5.0) class is used to specify that a property value must match a specified URL pattern. The DataForm component displays an error message if the property value does not match the specified URL pattern. 

{% tabs %}
{% highlight C# tabtitle="C#"  %}

[Url(ErrorMessage = "URL is not valid")]
public string Url { get; set; }

{% endhighlight %}
{% endtabs %}

### Enum data type attribute

The [EnumDataTypeAttribute](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.dataannotations.enumdatatypeattribute?view=net-5.0) class is used to specify that a property value must be a member of the specified enumeration. The DataForm component displays an error message if the property value is not a member of the specified enumeration. 

{% tabs %}
{% highlight C# tabtitle="C#"  %}

 [EnumDataType(typeof(Gender), ErrorMessage = "Please enter a valid gender")]
 public string Gender { get; set; }

{% endhighlight %}
{% endtabs %}

### Compare attribute

The [CompareAttribute](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.dataannotations.compareattribute?view=net-5.0) class is used to specify that a property value must match the value of another property in the same class. The DataForm component displays an error message if the property value does not match the value of the other property. 

{% tabs %}
{% highlight C# tabtitle="C#"  %}

[Compare("Password", ErrorMessage = "Passwords do not match")]
public string ConfirmPassword { get; set; }

{% endhighlight %}
{% endtabs %}

## Editable attribute

The [EditableAttribute](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.dataannotations.editableattribute?view=net-5.0) class is used to specify that a property can be edited in the DataForm component. 

{% tabs %}
{% highlight C# tabtitle="C#"  %}

[Editable(false)]
public string ID { get; set; }

{% endhighlight %}
{% endtabs %}

## Custom validation

A [custom validation attribute](https://learn.microsoft.com/en-us/previous-versions/aspnet/cc668224(v=vs.100)#creating-a-custom-validation-attribute) in .NET is a class that inherits from the [ValidationAttribute](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.dataannotations.validationattribute?view=net-8.0&redirectedfrom=MSDN) abstract class and overrides the [IsValid](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.dataannotations.validationattribute.isvalid?view=net-8.0#system-componentmodel-dataannotations-validationattribute-isvalid(system-object)) method. This method is called when the attribute is applied to a property and the property's value is being validated.

In the `IsValid` method, you can define your custom validation logic. If the validation fails, you return a [ValidationResult](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.dataannotations.validationresult?view=net-8.0) object with an error message. If the validation passes, you return `ValidationResult.Success`.

{% tabs %}
{% highlight razor tabtitle="Custom Validation Attributes"  %}

{% include_relative code-snippet\data-annotation-attributes\custom-validation.razor %}

{% endhighlight %}
{% endtabs %}

 In the above example, In the `PasswordValidationAttribute` class, the `IsValid` method checks if the password meets certain criteria (length, contains uppercase letter, contains lowercase letter, contains special character). If it doesn't, it returns a `ValidationResult` with an appropriate error message.In the `EmailValidationAttribute` class, the IsValid method checks if the email is in a valid format. If it's not, it returns a `ValidationResult` with an error message. 

![Blazor DataForm Custom Validation](images/blazor_dataform_customvalidation.png)