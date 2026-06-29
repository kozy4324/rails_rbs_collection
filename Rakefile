desc "rbs prototype rb tmp/rails/activerecord/lib/**/*.rb > generated/activerecord/8.1/generated.rbs"
task :prototype_activerecord do
  base = "tmp/rails/activerecord/lib/active_record"
  sh %|rbs prototype rb #{base}/attribute_methods/read.rb             >  generated/activerecord/8.1/generated.rbs|
  sh %|rbs prototype rb #{base}/attribute_methods/write.rb            >> generated/activerecord/8.1/generated.rbs|
  sh %|rbs prototype rb #{base}/attribute_methods/before_type_cast.rb >> generated/activerecord/8.1/generated.rbs|
  sh %|rbs prototype rb #{base}/attribute_methods/query.rb            >> generated/activerecord/8.1/generated.rbs|
  sh %|rbs prototype rb #{base}/attribute_methods/dirty.rb            >> generated/activerecord/8.1/generated.rbs|
  sh %|rbs prototype rb #{base}/scoping/named.rb                      >> generated/activerecord/8.1/generated.rbs|
  sh %|rbs prototype rb #{base}/persistence.rb                        >> generated/activerecord/8.1/generated.rbs|
end

desc "generated/activerecord/8.1/generated.rbs -> gems/activerecord/8.1/generated.rbs"
task rbs_patch_activerecord: [:prototype_activerecord] do
  sh %|rbs-patch generated/activerecord/8.1/generated.rbs generated/activerecord/8.1/patch.rbs > gems/activerecord/8.1/generated.rbs|
end

task activerecord: [:rbs_patch_activerecord]
task default: [:activerecord]
