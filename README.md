# Wall-area-problem
using constructors we calculate a wall area 

public class Wall {

    private double height;
    private double width;

    public Wall(double height, double width) {
        this.height = height;
        this.width = width;
    }

    public Wall() {
    }

    public double getHeight() {
        return this.height;
    }

    public double getWidth() {
        return this.width;
    }

    public double getArea(){
        if(this.width < 0 || this.height < 0){
            this.width = 0; this.height = 0;
        }
        return this.width * this.height;
    }

    public void setHeight(double height) {
        if(height < 0){
            this.height = 0;
        } else {
            this.height = height;
        }
    }

    public void setWidth(double width) {
        if(this.width < 0){
            this.width = 0;
        } else {
            this.width = width;
        }
    }
}

