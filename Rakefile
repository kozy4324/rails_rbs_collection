desc "rbs prototype rb tmp/rails/activerecord/lib/**/*.rb > gems/activerecord/8.1/generated.rbs"
task :activerecord do
  base = "tmp/rails/activerecord/lib/active_record"
  sh %|rbs prototype rb #{base}/attribute_methods/read.rb             >  gems/activerecord/8.1/generated.rbs|
  sh %|rbs prototype rb #{base}/attribute_methods/write.rb            >> gems/activerecord/8.1/generated.rbs|
  sh %|rbs prototype rb #{base}/attribute_methods/before_type_cast.rb >> gems/activerecord/8.1/generated.rbs|
  sh %|rbs prototype rb #{base}/attribute_methods/query.rb            >> gems/activerecord/8.1/generated.rbs|
  sh %|rbs prototype rb #{base}/attribute_methods/dirty.rb            >> gems/activerecord/8.1/generated.rbs|
  sh %|rbs prototype rb #{base}/scoping/named.rb                      >> gems/activerecord/8.1/generated.rbs|
  sh %|rbs prototype rb #{base}/persistence.rb                        >> gems/activerecord/8.1/generated.rbs|
end

task generate: [:activerecord]
task default: [:generate]
