desc "rbs prototype rb tmp/rails/activerecord/lib/**/*.rb > gems/activerecord/8.1/generated.rbs"
task :activerecord do
  # sh %|rbs prototype rb tmp/rails/activerecord/lib/active_record/base.rb > gems/activerecord/8.1/generated.rbs|
  sh %|echo "module ActiveRecord       end" >  gems/activerecord/8.1/generated.rbs|
  sh %|echo "class  ActiveRecord::Base end" >> gems/activerecord/8.1/generated.rbs|

  sh %|rbs prototype rb tmp/rails/activerecord/lib/active_record/attribute_methods/read.rb >> gems/activerecord/8.1/generated.rbs|
  sh %|rbs prototype rb tmp/rails/activerecord/lib/active_record/scoping/named.rb >> gems/activerecord/8.1/generated.rbs|
end

task generate: [:activerecord]
