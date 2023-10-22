# C# - Interface（インターフェース）

## 概要

C#のインターフェースは、メソッド、プロパティ、イベント、インデクサのシグニチャを定義することができる契約のようなものです。インターフェース自体は実装を持たず、それを実装するクラスや構造体にその実装を提供する義務があります。

## なぜインターフェースを使用するのか？

- **振舞い方の提供**: インターフェースは、あるクラスが実装すべきメソッドやプロパティのどう振る舞うかを定義します。
- **多重継承**: C#はクラスの多重継承をサポートしていませんが、複数のインターフェースを実装することで、多重継承のような振る舞いを模倣することができます。

## 例

```csharp
public interface IDriveable
{
    void Drive();
}

public class Car : IDriveable
{
    public void Drive()
    {
        Console.WriteLine("Car is driving.");
    }
}

public class Truck : IDriveable
{
    public void Drive()
    {
        Console.WriteLine("Truck is driving.");
    }
}


