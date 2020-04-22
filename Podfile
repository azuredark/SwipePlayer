# Uncomment the next line to define a global platform for your project
# platform :ios, '9.0'

target 'test2' do
  # Comment the next line if you're not using Swift and don't want to use dynamic frameworks
  use_frameworks!

  # Pods for test2
  pod "SnapKit"
  pod "YetAnotherAnimationLibrary"

end

post_install do |installer|
    installer.pods_project.targets.each do |target|
      
        target.build_configurations.each do |config|
          config.build_settings['LD_NO_PIE'] = 'NO'
        end

        if ['YetAnotherAnimationLibrary'].include? target.name
            target.build_configurations.each do |config|
                config.build_settings['SWIFT_VERSION'] = '4.2'
            end
        end
    end
end
