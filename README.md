# Functional_Interfaces_for_Primitives_By_Alin

//Common functional interfaces for primitives

        //"Primitive"Supplier
        //"primitive" getAs"Primitive"()
        //generate "primitive" without taking any input. [0 parameters]

        //BooleanSupplier   boolean getAsBoolean()
        //getAsBoolean(generate,supply) result(boolean) without taking any input.
        //Only functional interface for boolean.

        //DoubleSupplier    double getAsDouble()
        //getAsDouble(generate,supply) result(double) without taking any input.

        //IntSupplier       int getAsInt()
        //getAsInt(generate,supply) result(int) without taking any input.

        //LongSupplier      long getAsLong()
        //getAsLong(generate,supply) result(long) without taking any input.

        //_____________________________________________________________________________

        //"Primitive"Consumer
        //void accept("primitive")
        //do something with (accept) a parameter("primitive") but not return anything.

        //DoubleConsumer    void accept(double)
        //do something with (accept) a parameter(double) but not return anything.

        //IntConsumer       void accept(int)
        //do something with (accept) a parameter(int) but not return anything.

        //LongConsumer      void accept(long)
        //do something with (accept) a parameter(long) but not return anything.

        //_____________________________________________________________________________

        //"Primitive"Predicate
        //boolean test("primitive")
        //return a boolean and takes a "primitive".

        //DoublePredicate    boolean test(double)
        //DoublePredicate has one method named test(true or false) that returns a boolean and takes a double.

        //IntPredicate       boolean test(int)
        //IntPredicate has one method named test(true or false) that returns a boolean and takes an int.

        //LongPredicate      boolean test(long)
        //LongPredicate has one method named test(true or false) that returns a boolean and takes a long.

        //_____________________________________________________________________________

        //"Primitive"Function<Returntype>
        //Returntype apply("primitive")
        //change(apply) (use) one parameter("primitive") into a value and returning it.
        //return value can be a different type.

        //DoubleFunction<Returntype>       Returntype apply(double);
        //change(apply) (use) one parameter(double) into a value and returning it
        //return value can be a different type

        //IntFunction<Returntype>           Returntype apply(int);
        //change(apply) (use) one parameter(int) into a value and returning it
        //return value can be a different type

        //LongFunction<Returntype>          Returntype apply(long);
        //change(apply) (use) one parameter(long) into a value and returning it
        //return value can be a different type

        //_____________________________________________________________________________

        //"Primitive"UnaryOperator
        //"primitive" applyAs"Primitive"("primitive")
        //change (applyAs"Primitive") (use) one parameter("primitive") into a value("same primitive") and returning it
        //return value must be the same type.

        //DoubleUnaryOperator     double applyAsDouble(double)
        //change (applyAsDouble) (use) one parameter(double) into a value(double) and returning it
        //return value must be the same type

        //IntUnaryOperator        int applyAsInt(int)
        //change (applyAsInt) (use) one parameter(int) into a value(int) and returning it
        //return value must be the same type

        //LongUnaryOperator       long applyAsLong(long)
        //change (applyAsLong) (use) one parameter(long) into a value(long) and returning it
        //return value must be the same type

        //_____________________________________________________________________________

        //"Primitive"BinaryOperator
        //"primitive" applyAs"Primitive"("primitive", "same primitive")
        //change (applyAs"Primitive") (use) two parameters("primitive", "same primitive") into a value("same primitive") and returning it
        //both parameters and return value must be the same type

        //DoubleBinaryOperator    double applyAsDouble(double, double)
        //change (applyAsDouble) (use) two parameters(double, double) into a value(double) and returning it
        //both parameters and return value must be the same type

        //IntBinaryOperator       int applyAsInt(int, int)
        //change (applyAsInt) (use) two parameters(int, int) into a value(int) and returning it
        //both parameters and return value must be the same type

        //LongBinaryOperator      long applyAsLong(long, long)
        //change (applyAsLong) (use) two parameters(long, long) into a value(long) and returning it
        //both parameters and return value must be the same type

        //_____________________________________________________________________________

        //There are a few things to notice that are different:

        //Generics are gone from all of the interfaces except "Primitive"Function<Returntype>,
        //because the type name tells us what primitive type is involved.
        //In other cases, such as IntFunction, only the return type generic is needed.
        //The single abstract method is often, but not always, renamed to reflect the primitive type involved.
        //(As"Primitive" este in plus la nume).
        //BiConsumer, BiPredicate, and BiFunction are not in here.
        //The API designers stuck to the most common operations.
        //For primitives, the functions with two different type parameters just aren't used often.

        //In addition to equivalents, some interfaces are specific to primitives.
        //Primitive-specific functional interfaces

        //To"Primitive"Function<Type>
        //"primitive" applyAs"Primitive"(Type);
        //change(applyAs"Primitive") (use) one parameter(Type) into a value("primitive") and returning it.

        //ToDoubleFunction<Type>      double applyAsDouble(Type);
        //change(applyAsDouble) (use) one parameter(Type) into a value(double) and returning it.

        //ToIntFunction<Type>         int applyAsInt(Type);
        //change(applyAsInt) (use) one parameter(Type) into a value(int) and returning it.

        //ToLongFunction<Type>        long applyAsLong(Type);
        //change(applyAsLong) (use) one parameter(Type) into a value(long) and returning it.

        //_____________________________________________________________________________

        //To"Primitive"BiFunction<Type, Different Type U>
        //"primitive" applyAs"Primitive"(Type, Different Type U);
        //change two parameters into a value("primitive") and returning it.
        //Parameters don’t have to be the same type.
        //To"Primitive"BiFunction can use the same type for both the T and U generic parameters.

        //ToDoubleBiFunction<Type, Different Type U>     double applyAsDouble(Type, Different Type U);
        //change two parameters into a value(double) and returning it.
        //Parameters don’t have to be the same type.
        //ToDoubleBiFunction can use the same type for both the T and U generic parameters.

        //ToIntBiFunction<Type, Different Type U>        int applyAsInt(Type, Different Type U);
        //change two parameters into a value(int) and returning it.
        //Parameters don’t have to be the same type.
        //ToIntBiFunction can use the same type for both the T and U generic parameters.

        //ToLongBiFunction<Type, Different Type U>       long applyAsLong(Type, Different Type U);
        //change two parameters into a value(long) and returning it.
        //Parameters don’t have to be the same type.
        //ToLongBiFunction can use the same type for both the T and U generic parameters.

        //_____________________________________________________________________________

        //"Primitive"To"OtherPrimitive"Function
        //"otherprimitive" applyAs"OtherPrimitive"("primitive")
        //change(applyAs"OtherPrimitive") (use) one parameter("primitive") into a value("otherprimitive") and returning it.

        //DoubleToIntFunction        int applyAsInt(double)
        //change(applyAsInt) (use) one parameter(double) into a value(int) and returning it.

        //DoubleToLongFunction       long applyAsLong(double)
        //change(applyAsLong) (use) one parameter(double) into a value(long) and returning it.

        //IntToDoubleFunction        double applyAsDouble(int)
        //change(applyAsDouble) (use) one parameter(int) into a value(double) and returning it.

        //IntToLongFunction          long applyAsLong(int)
        //change(applyAsLong) (use) one parameter(int) into a value(long) and returning it.

        //LongToDoubleFunction       double applyAsDouble(long)
        //change(applyAsDouble) (use) one parameter(long) into a value(double) and returning it.

        //LongToIntFunction          int applyAsInt(long)
        //change(applyAsInt) (use) one parameter(long) into a value(int) and returning it.

        //_____________________________________________________________________________

        //Obj"Primitive"Consumer<Type>
        //void accept(Type , "primitive")
        //do something with (accept) (consume,use) two parameters(Type, "primitive") but not return anything.

        //ObjDoubleConsumer<Type>     void accept(Type , double)
        //do something with (accept) (consume,use) two parameters(Type, double) but not return anything.

        //ObjIntConsumer<Type>        void accept(Type , int)
        //do something with (accept) (consume,use) two parameters(Type, int) but not return anything.

        //ObjLongConsumer<Type>       void accept(Type , long)
        //do something with (accept) (consume,use) two parameters(Type, long) but not return anything.
 
