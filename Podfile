# Uncomment the next line to define a global platform for your project
# platform :ios, '9.0'

def shared_pods
  pod 'Realm'
  pod 'RealmLoginKit'
end

target 'RealmPuzzle' do
  use_frameworks!
  shared_pods
end

target 'RealmPuzzleTests' do
  use_frameworks!
  shared_pods
end

post_install do |installer|
    installer.pods_project.targets.each do |target|
        target.build_configurations.each do |config|
            config.build_settings['SWIFT_VERSION'] = '3.0'
        end
    end
  end
