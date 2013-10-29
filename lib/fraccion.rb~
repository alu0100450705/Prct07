#raiz= ""
# path = File.dirname(__FILE__)
# require "#{path}/gcd.rb"
require "./gcd.rb"
class Fraccion
   include Comparable
   attr_reader :num, :den # metodos de acceso (getters)

   #Incializacion de las variables de clase
   def initialize(num, den)
      @num, @den = num, den
      aux = gcd(num,den)
      @num = num / aux
      @den = den / aux
   end

	  #Metodo de impresion por pantalla
   def to_s
      if (@num < 0) and (@den < 0)
         "#{@n.abs}/#{@d.abs}"
      else
         "#{@num}/#{@den}"
      end
   end
  
  #comparador
   def == (other)
      if (@num == other.num) and (@den == other.den)
         return true
      else
							return falsef1=@num/@den
      end
   end
	
	  #Valor absoluto
   def abs
      Fraccion.new(@num.abs,@den.abs)
   end
  
  #valor reciproco
   def reciprocal 
      Fraccion.new(@den,@num)
   end
  
  #opuesto de una fraccion
   def -@
      Fraccion.new(-@num,-@den)
   end

	  #en formato flotante
   def to_f
      fl=@num/@den
   end

   #Suma de racionales
   def +(other)
      if (@den==other.den)   #si los denominadores son iguales
         Fraccion.new(@num+other.num,@den)
      else  #si los denominadores son distintos
         Fraccion.new( ( (@num*other.den ) + ( @den*other.num) ),@den*other.den)
      end
   end
			
			#Resta de racionales
   def -(other)
      if (@den==other.den)   #si los denominadores son iguales
         Fraccion.new(@num-other.num,@den)
      else  #si los denominadores son distintos
         Fraccion.new( ( (@num*other.den ) - ((@den)*other.num ) ),@den*other.den)
						end
	  end

   #producto de un racional por otro racional
   def *(other)
      Fraccion.new(@num*other.num,@den*other.den)
   end

   def / (other)
      Fraccion.new(@num*other.den ,@den*other.num)
   end
	
   def % (other)
      frac3 = Fraccion.new(@num*other.den ,@den*other.num)
      Fraccion.new(frac3.num % frac3.den,1)
   end

   def < (other)
      fl=@num/@den
      fl1= other.num/other.den
      fl < fl1
   end

   def  > (other)
      fl=@num/@den
      fl1= other.num/other.den
      fl > fl1
   end

   def  >= (other)
      fl=@num/@den
      fl1= other.num/other.den
      fl >= fl1
   end

   def <= (other)
      fl=@num/@den
      fl1= other.num/other.den
      fl <= fl1
   end

end

