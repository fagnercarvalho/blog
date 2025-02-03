+++
date = '2014-10-26'
title = 'Null propagator operator on C# 6.0'
categories = ["programming", "csharp"]
+++

Hello again! Today I'm going to talk briefly about a specific feature from the next version of C#: the not so new null propagator operator. Yes, its been awhile since C# 6 was announced but I want to talk about this, so you cant do anything to stop me!
The main reason I'm talking about this it's because since I saw the [proposal](https://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/3990187-add-operator-to-c) for implementing the operator in C# I really liked and hoped that Microsoft implement, and he did it! In the latest Visual Studio 2014 CTP version the operator was there and of course I looked. Verdict: tested and approved!

#### Null propagator operator?

So, in the first place, this operator is new only in C#. A lot of programming languages already have it.
Like [Damien Guard](http://damieng.com/blog/2013/12/09/probable-c-6-0-features-illustrated) pointed out this operator  exists in [Groovy](http://groovy.codehaus.org/Operators#Operators-SafeNavigationOperator%28?.%29), where is known as the 'safe navigation operator', that bring me to right to the usefulness of this operator: avoid Null reference exception when trying to access a null reference object, of course!
But how this is done? You all know how to do a null reference exception in your code, everyone does that once in a while. Yes, is stupid but it happens, and the new null propagator operator comes here to solve this once and for all.

Like Linus said someday: 'Talk is cheap. Show me the code'. So, there it is:

{{< gist fagnercarvalho 75e62ba490db8ea8f0f0 null-propagator-operator.cs >}}

The new operator is shown in line 14, where its used two times. So, what happens if the Bear object has not instantiated? Or the Friends property? If you dont use the null propagator you probably get a null reference exception in your face. But in the code above this wont happen again.

#### So, why?

Why you need to use this new operator? Well, because is simple and avoids a lot of boilerplate that just messes with your code. Its simple as that.

#### I love it, how can I start using it?

The new operator isn't available in a stable C# version yet. But you can test right now using the latest version of Visual Studio 2014. And you dont need to install in your machine, Microsoft already offers a Windows Server 2013 instance with Visual Studio 2014 CTP 4 pre-installed. You just needed to access [manage.windowsazure.com](http://manage.windowsazure.com), create a new VS 2014 VM and starting using the new Visual Studio and C# features. If you are interested in all the new features in C# 6.0 I recommend you take a look in [this](https://roslyn.codeplex.com/discussions) and [this](https://channel9.msdn.com/tags/CSharp/).

So, that's it! If you have any questions you are free to ask in the commentary box below.

Bye!
