require 'rspec'
#path = File.dirname(__FILE__)  #path relativo
# Dir.chdir "../lib/"
require "lib/fraccion.rb"

describe Fraccion do

   before :each do
      @frac = Fraccion.new(5,2)
   end    

   describe "# Debe exitir un " do
      it "numerador" do
         defined?(@frac.num) 
      end

      it "denominador" do
         defined?(@frac.den)
      end
   end
  
   describe "Debe estar en " do
      it "forma reducida" do
         @frac2 = Fraccion.new(10,4)
         @frac2.num.should eq(5)
         @frac2.den.should eq(2)
      end
   end
  
   describe "Se debe invocar al " do
      it "metodo num() para obtener al numerador" do
         @frac.num.should eq @frac.num()
      end

      it "metodo den() para obtener al denominador" do
         @frac.den.should eq @frac.den()
      end
   end
  
   describe "Se Debe mostrar por consola la fraccion en formato " do
      it " a/b  donde a en el numerador y b es el numerador" do
         aux = @frac.to_s
         aux[0].to_i.should eq (@frac.num)
         aux[2].to_i.should eq (@frac.den)
      end
      #Hacer el procedimineto flotante generico
      it "  flotante" do
         @resultado=@frac.to_f
         @resultado_esperado= @frac.num / @frac.den
         @resultado.should eq(@resultado_esperado)  #cambio el .to_i por to_f
      end
   end
 
   describe "Se debe comparar  " do
      it " si dos fracciones son iguales" do
         @frac2 = Fraccion.new(5,2)
         (@frac == @frac2).should eq (true)
      end

      it " si dos fracciones son diferentes" do
         @frac2 = Fraccion.new(6,2)
         (@frac == @frac2).should eq (false)
      end
   end
  
   describe "Se debe calcular  " do
      it " Valor absoluto con el metodo ABS" do
         @frac2 = Fraccion.new(-9,-5)
         fracx = @frac2.abs
         fracx.num.should eq (9)
         fracx.den.should eq (5)
      end

      it " Reciproco con el metodo reciprocal" do
         @frac2 = Fraccion.new(4,3)
         fracx = @frac2.reciprocal
         fracx.num.should eq (3)
         fracx.den.should eq (4)
      end

      it " el opuesto con -" do
         frac2 = - @frac
         frac2.num.should eq (-5)
         frac2.den.should eq (-2)
      end
   end

   describe "Se debe " do
      it "sumar dos fracciones con + y dar el resultado de forma reducida" do
         frac2= Fraccion.new(1,2)
         frac3= @frac + frac2
						
									if (frac3.num==3)and(frac3.den==1)
									   dev=true
									else
										  dev=false
									end
									dev.should be_true  #solo pasa la prueba si dev es true
								end

						it "restar dos fracciones con - y dar el resultado de forma reducida" do
         frac2= Fraccion.new(1,2)
							  frac3= @frac - frac2
							  if (frac3.num==2)and(frac3.den==1)
								    dev=true
							  else
								    dev=false
							  end
									dev.should be_true
						end

						it "multiplicar dos fracciones con * y dar el resultado de forma reducida" do
         frac2=Fraccion.new(1,2)
									frac3= @frac * frac2
									if (frac3.num==5)and(frac3.den==4)
									   dev=true
									else
									   dev=false
									end
									(dev.should_not be_nil) and(dev.should be_true) #dev no puede ser nil y ademas debe ser true
						end

						it "dividir dos fracciones con / y dar el resultado de forma reducida" do
						   frac2=Fraccion.new(1,2)
						   frac3= @frac / frac2
						   if (frac3.num==5)and(frac3.den==1)   # 5/1=5
							     dev=true
							  else
								    dev=false
							  end
									valor=frac3.num / frac3.den
							  (dev.should_not be_nil) and (dev.should be_true) and (dev.should be_close(valor,0.5)) #dev no puede ser nil y ademas debe ser true
						end

						it "calcular el resto dos fracciones con % y dar el resultado de forma reducida" do
						   frac2=Fraccion.new(1,2)
						   frac3= @frac % frac2
									if (frac3.num==0)and(frac3.den==0)
									   dev=true
									else
									   dev=false
									end
									(dev.should_not be_nil) and (dev.should be_true)
						end

			end
			
	describe "Se debe comparar  " do
      it " si una fracion es menor que otra" do
         @frac2 = Fraccion.new(1,2)
         (@frac2 < @frac).should eq (true)
      end

      it " si una fracion es mayor que otra" do
        @frac2 = Fraccion.new(7,2)
         (@frac2 > @frac).should eq (true)
      end
      
      it " si una fracion es mayor o igual" do
        @frac2 = Fraccion.new(5,2)
         (@frac2 >= @frac).should eq (true)
      end
      
       it " si una fracion es menor o igual" do
         @frac2 = Fraccion.new(5,2)
         (@frac2 <= @frac).should eq (true)
      end
   end
	
end
  
