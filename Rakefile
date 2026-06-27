desc "rbs prototype rb tmp/rails/activerecord/lib/**/*.rb > gems/activerecord/8.1/generated.rbs"
task :generate_activerecord do
  sh %|rbs prototype rb tmp/rails/activerecord/lib/**/*.rb > gems/activerecord/8.1/generated.rbs|
end

desc "rbs prototype rb tmp/rails/activemodel/lib/**/*.rb > gems/activemodel/8.1/generated.rbs"
task :generate_activemodel do
  sh %|rbs prototype rb tmp/rails/activemodel/lib/**/*.rb > gems/activemodel/8.1/generated.rbs|
end

task generate: [:generate_activerecord, :generate_activemodel]
