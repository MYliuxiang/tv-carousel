# tv-carousel
使用
****
``` 
$ yarn install tv-carousel
```
```javascript
import Carousel from 'tv-carousel';

export class MyCarousel extends Component {

    _renderItem = ({item, index}) => {
        return (
            <View style={styles.slide}>
                <Text style={styles.title}>{ item.title }</Text>
            </View>
        );
    }

    render () {
        return (
            <Carousel
              ref={(c) => { this._carousel = c; }}
              data={this.state.entries}
              renderItem={this._renderItem}
              sliderWidth={300}
              itemWidth={300}
            />
        );
    }
}
```

