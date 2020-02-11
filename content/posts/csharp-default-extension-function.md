---
title: "Csharp Default Extension Function"
date: 2020-02-11T09:38:05+09:00
draft: false
---

#### 형변환 확장 함수
~~~
public static class ExtensionMethods
{
    public static int ToInt(this string value, int defaultInteger = 0)
    {
        try
        {
            if (int.TryParse(value, out int validInteger))
                return validInteger;
            else
                return defaultInteger;
        }
        catch
        {
            return defaultInteger;
        }
    }

    public static decimal ToDecimal(this string value, decimal defaultDecimal = 0.0M)
    {
        try
        {
            if (decimal.TryParse(value, out decimal validDecimal))
                return validDecimal;
            else
                return defaultDecimal;
        }
        catch
        {
            return defaultDecimal;
        }
    }

    public static double ToDouble(this string value, double defaultDouble = 0.0D)
    {
        try
        {
            if (double.TryParse(value, out double validDouble)) // Out variables
                return validDouble;
            else
                return defaultDouble;
        }
        catch
        {
            return defaultDouble;
        }
    }
}
~~~