# -*- coding: utf-8 -*-
task :default => :bin

desc "Ejecutar el código de la clase Fraccion"
   task :bin do
      sh "ruby ./lib/fraccion.rb"
end

desc "Ejecutar test con documentacion"
   task :test do
      sh "rspec -I. spec/fraccion_spec.rb --format documentation"
end

desc "Ejecutar test en formato html"
   task :thtml do
      sh "rspec -I. spec/fraccion_spec.rb --format html > resultado.html"
						sh "firefox resultado.html&"
end
